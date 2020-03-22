<apex:page standardController="Contact" extensions="CandidateRegistrationApex" showHeader="true" docType="html-5.0">
    <!-- Page Header -->
    <center><h3>CANDIDATE REGISTRATION FORM</h3></center>
    <!-- Begin Form -->
    <apex:form id="form1" title="Candidate Registration Form" styleClass="form1">
        <apex:pageMessages />
        <apex:pageBlock >
            <!-- Personal Info -->
            <apex:outputPanel layout="block" styleClass="custom1">
                <apex:pageBlockSection title="Personal Introduction" columns="2"> 	
                    <apex:inputField value="{!Contact.FirstName}" />     
                    <apex:inputField value="{!Contact.MobilePhone}"  /> 
                    <apex:inputField value="{!Contact.LastName}" />
                    <apex:inputField value="{!Contact.Birthdate}" showDatePicker="true"/>
                    <apex:inputField value="{!Contact.Email}" />
                    <apex:inputField value="{!Contact.Marital_Status__c}" />  
                    <apex:inputField value="{!Contact.Are_you_physically_Challenged__c}" />
              <apex:inputField value="{!Contact.Applying_for_position_of__c }" required="true"/>
                        <!--    <apex:selectList multiselect="false" size="1" styleClass="picklist2" label="Applying for Position" required="true">-->
                    <apex:selectOption itemLabel="Applying for" itemValue="Applying for"/>
                         <!--     <apex:selectOptions value="{!ApplyingPickList}"  />  </apex:selectList> -->
                    <apex:inputField value="{!Contact.Linkedln_URL__c}" />
                     <apex:inputField value="{!Contact.Google_drive_Link__c}" />
                   </apex:pageBlockSection></apex:outputPanel>
            
            
            <!--Address Section-->
            <apex:outputPanel layout="block" styleClass="custom1">
                <apex:pageBlockSection title="Address Details" columns="2"> 
                    <apex:inputText value="{!Contact.Street__c}" label="Street" /> 
                    <apex:inputField value="{!Contact.State_Province__c}" label="State/Province" />
                    <apex:inputField value="{!Contact.City__c}" label="City"/>
                    <apex:inputText value="{!Contact.Country__c}" label="Country" /> 
                    <apex:inputField value="{!Contact.Postal_Code__c}" label="PostalCode"/>
                </apex:pageBlockSection></apex:outputPanel>
            
            
            <!--Education Section-->
            <apex:outputPanel layout="block" styleClass="custom1">
              
                    <apex:pageBlockSection title="Graduation Details" columns="2">
                        <apex:inputField value="{!Contact.Graduation__c}" /> 
                        <apex:inputField value="{!Contact.Institute_Name_and_Location__c}" />
                        <apex:inputField value="{!Contact.G_Starting_Year__c}" showDatePicker="true" />
                        <apex:inputField value="{!Contact.GPassing_Year__c}" showDatePicker="true" />
                        <apex:inputField value="{!Contact.CGPA_or_Percentage__c}" />
                    </apex:pageBlockSection>
                    <apex:pageBlockSection title=" Post-Graduation Details" columns="2">
                        <apex:inputField value="{!Contact.Post_graduation__c}" />
                        <apex:inputField value="{!Contact.P_Institute_Name_location__c}" />
                         <apex:inputField value="{!Contact.P_Starting_Year__c}" showDatePicker="true" />
                        <apex:inputField value="{!Contact.P_Passing_Year__c}" showDatePicker="true" />
                        <apex:inputField value="{!Contact.P_CGPA_or_Percentage__c}" />
                    </apex:pageBlockSection>
               </apex:outputPanel>
            
            <!-- CHECKBOX FOR EXPERIENCE --> 
            <!--Experience
<apex:outputPanel layout="block" styleClass="custom4">
<apex:pageBlockSection title="Are you experienced" id="abc" columns="2">
<apex:actionRegion >Experience<apex:inputCheckbox value="{!Contact.Experience__c}"> 
<apex:actionSupport event="onclick" reRender="psg1,abc"/>
</apex:inputCheckbox></apex:actionRegion></apex:pageBlockSection>

<apex:pageBlockSection id="psg1">
<apex:inputField value="{!Contact.Previous_Company_Name__c}" rendered="{!Contact.Experience__c}" />
<apex:inputField value="{!Contact.Year_Of_Experience__c}" rendered="{!Contact.Experience__c}"/>
<apex:inputField value="{!Contact.Current_Location__c}" rendered="{!Contact.Experience__c}" />
<apex:inputField value="{!Contact.Location_Preference__c}" rendered="{!Contact.Experience__c}" />
<apex:inputField value="{!Contact.Reason_for_change__c}" rendered="{!Contact.Experience__c}"/>
<apex:inputField value="{!Contact.Current_CTC__c}" rendered="{!Contact.Experience__c}"/>
<apex:inputField value="{!Contact.Expected_CTC__c}" rendered="{!Contact.Experience__c}"/>
</apex:pageBlockSection></apex:outputPanel>-->
            
            <!--Experience-->
            <apex:outputPanel layout="block" styleClass="custom1">
                <apex:pageBlockSection title="Experience" columns="2">
                    
                    <apex:inputField value="{!Contact.Previous_Company_Name__c}" />
                    <apex:inputField value="{!Contact.Year_Of_Experience__c}"/>
                    <apex:inputField value="{!Contact.Current_Location__c}" />
                    <apex:inputField value="{!Contact.Location_Preference__c}" />
                    <apex:inputField value="{!Contact.Reason_for_change__c}"/>
                    <apex:inputField value="{!Contact.Designation__c}"/>
                    <apex:inputField value="{!Contact.Current_CTC__c}"/>
                    <apex:inputField value="{!Contact.Expected_CTC__c}"/>
                    <!--   <apex:inputfield value="{!Contact.Comments__c}"/> -->
                </apex:pageBlockSection></apex:outputPanel>
            
            <!--Skill Set Code-->
            <apex:outputPanel layout="block" styleClass="custom1">
                <apex:pageBlockSection title="Skill Set" columns="2">
                    <apex:inputField value="{!Contact.IT_Skills__c}" />
                    <apex:inputField value="{!Contact.Certifications__c}" />
                </apex:pageBlockSection></apex:outputPanel>
            
            <!--Cv upload-->
            <!--apex:outputPanel layout="block" styleClass="custom6">
                <apex:pageBlockSection title="CV Details">
                    <b><center>Please Upload Your Recent CV</center></b>
                    
                    <apex:inputFile value="{!file}" />
                    <center><apex:commandbutton action="{!upload}" value="Upload"/></center>
                </apex:pageBlockSection></apex:outputPanel-->
            
<!--<apex:inputField value="{!Contact.CV_Upload__c}" label="CV Upload" />-->            
            <!-- Description Section 
<apex:outputPanel layout="block" styleClass="custom7">
<apex:pageBlockSection title="Description" columns="2">
<apex:inputField value="{!Contact.Description}" />
</apex:pageBlockSection></apex:outputPanel> -->
            
            
            
            <!-- Button Section -->
            <apex:outputPanel layout="block" styleClass="custom1">
                <apex:pageBlockSection >
                    <center><apex:actionRegion ><apex:commandButton value="Submit" action="{!saveRecord}" styleClass="button1"/> </apex:actionRegion></center>
                </apex:pageBlockSection> </apex:outputPanel>
        </apex:pageBlock>
    </apex:form>

<apex:form id="form2" title="Candidate Registration Form" styleClass="form1">
    <apex:outputPanel layout="block" style="background-color:#66ffd9">
    <apex:pageblock >
            <apex:commandbutton onclick="this.value = 'Authenticating....'" action="{!DriveAuth}" value="Google Drive Authentication">
            </apex:commandbutton>
            <br/>
            <apex:inputfile value="{!file}" contentType="{!filetype}" filename="{!filename}" />
            <br/>
            <apex:commandButton onclick="this.value = 'Uploading...'" value="Upload file" action="{!UploadFile}" />
            <br/>
            <apex:messages styleClass="error" />
            <br/>
            </apex:pageblock>
    </apex:outputPanel>
    </apex:form>    
    <!-- Javascript for Date datatype -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/css/bootstrap.min.css" />
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.0/js/bootstrap.min.js"></script>
    <apex:includeScript value="https://ajax.googleapis.com/ajax/libs/jquery/1.4.2/jquery.min.js"></apex:includeScript>
    <span id="hideMyParent"></span>
    
    <script type="text/javascript"> $(document).ready(function() { 
    var startYear=1970; 
    var endYear=2019; 
    var optionsString=''; 
    if(startYear<endYear){
        for(i=startYear;i<endYear+1;i++){ 
            optionsString += "<option value=\""+i+"\">"+i+"</option>"; 
        }
        $('#calYearPicker').html(optionsString); } $('#sidebarDiv #hideMyParent').parent().parent().hide();});
    </script> 
    
    <style>
        .button1:hover
        {
        background-color:blue;
        transform: scale(1.3);
        }
        .form1
        {
        margin-top: 40px;
        margin-bottom: 70px;
        margin-right: 150px;
        margin-left: 150px;
        border-style: solid;
        border-width: 5px 5px 5px 5px;
        }
         
        .custom1 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        }   
        .custom2 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        }  
        .custom3 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        }  
        .custom4 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        }  
        .custom5 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        } 
        .custom6 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        } 
        .custom7 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        } 
        .custom8 .pbSubheader {
        color: white !important;
        background-color:#151627 !important;
        } 
        .custom1 {
        background-color:#66ffd9;
        }
        .custom2 {
        background-color:#66ffd9;
        }
        .custom3 {
        background-color:#66ffd9;
        }
        .custom4 {
        background-color:#66ffd9;
        }
        .custom5 {
        background-color:#66ffd9;
        }
        .custom6 {
        background-color:#66ffd9;
        }
        .custom7 {
        background-color:#66ffd9;
        }
        .custom8 {
        background-color:#66ffd9;
        }
    </style>
</apex:page>
