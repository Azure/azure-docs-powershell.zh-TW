---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968797"
---
# <span data-ttu-id="f439c-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f439c-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="f439c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f439c-102">SYNOPSIS</span></span>
<span data-ttu-id="f439c-103">在虛擬機器上配置 DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="f439c-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="f439c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f439c-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f439c-105">說明</span><span class="sxs-lookup"><span data-stu-id="f439c-105">DESCRIPTION</span></span>
<span data-ttu-id="f439c-106">AzureVMDscExtension Cmdlet 會在虛擬機器上設定所需的狀態 **設定** (DSC) 延伸。</span><span class="sxs-lookup"><span data-stu-id="f439c-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="f439c-107">示例</span><span class="sxs-lookup"><span data-stu-id="f439c-107">EXAMPLES</span></span>

### <span data-ttu-id="f439c-108">範例1：在虛擬機器上設定 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="f439c-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="f439c-109">這個命令會在虛擬機器上配置 DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="f439c-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="f439c-110">使用 **AzureVMDscConfiguration** 命令之前，您必須先將 MyConfiguration.ps1.zip 套件上傳到 Azure 儲存空間，並包含 MyConfiguration.ps1 腳本和它所依賴的模組。</span><span class="sxs-lookup"><span data-stu-id="f439c-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="f439c-111">MyConfiguration 引數指明要執行的腳本內的特定 DSC 設定。</span><span class="sxs-lookup"><span data-stu-id="f439c-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="f439c-112">- *ConfigurationArgument* 參數會指定含有傳遞到設定函數之引數的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="f439c-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="f439c-113">範例2：使用配置資料的路徑來設定虛擬機器上的 DSC 延伸</span><span class="sxs-lookup"><span data-stu-id="f439c-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="f439c-114">這個命令會使用配置資料的路徑，在虛擬機器上配置 DSC 延伸。</span><span class="sxs-lookup"><span data-stu-id="f439c-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="f439c-115">參數</span><span class="sxs-lookup"><span data-stu-id="f439c-115">PARAMETERS</span></span>

### <span data-ttu-id="f439c-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="f439c-116">-ConfigurationArchive</span></span>
<span data-ttu-id="f439c-117">指定先前透過 Publish AzureVMDscConfiguration 上傳)  ( .zip 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f439c-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="f439c-118">這個參數必須只指定檔案名，不含任何路徑。</span><span class="sxs-lookup"><span data-stu-id="f439c-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="f439c-119">-ConfigurationArgument</span></span>
<span data-ttu-id="f439c-120">指定一個 hashtable，指定設定函數的引數。</span><span class="sxs-lookup"><span data-stu-id="f439c-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="f439c-121">鍵會對應到參數名稱和參數值的值。</span><span class="sxs-lookup"><span data-stu-id="f439c-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="f439c-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f439c-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f439c-123">基本類型</span><span class="sxs-lookup"><span data-stu-id="f439c-123">primitive types</span></span>
- <span data-ttu-id="f439c-124">字串</span><span class="sxs-lookup"><span data-stu-id="f439c-124">string</span></span>
- <span data-ttu-id="f439c-125">陣列</span><span class="sxs-lookup"><span data-stu-id="f439c-125">array</span></span>
- <span data-ttu-id="f439c-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="f439c-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="f439c-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="f439c-128">指定 psd1 檔案的路徑，該檔案會指定 configuration 函數的資料。</span><span class="sxs-lookup"><span data-stu-id="f439c-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="f439c-129">此檔案必須包含一個雜湊表，如分隔配置和環境資料中所述 https://msdn.microsoft.com/en-us/PowerShell/DSC/configData 。</span><span class="sxs-lookup"><span data-stu-id="f439c-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f439c-130">-ConfigurationName</span></span>
<span data-ttu-id="f439c-131">指定由 DSC 副檔名呼叫的配置腳本或模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f439c-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="f439c-132">這個參數的值必須是包含在 *ConfigurationArchive* 中的腳本或模組中的其中一個配置函數的名稱。</span><span class="sxs-lookup"><span data-stu-id="f439c-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="f439c-133">如果您省略此參數（不含任何副檔名），這個 Cmdlet 會預設為 *ConfigurationArchive* 參數所提供的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f439c-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="f439c-134">例如，如果 *ConfigurationArchive* 是「SalesWebSite.ps1.zip」，則 *ConfigurationName* 的預設值為「SalesWebSite」。</span><span class="sxs-lookup"><span data-stu-id="f439c-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-135">-容器</span><span class="sxs-lookup"><span data-stu-id="f439c-135">-ContainerName</span></span>
<span data-ttu-id="f439c-136">指定 *ConfigurationArchive* 所在之 Azure 儲存體容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f439c-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="f439c-137">-DataCollection</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-138">-Force</span><span class="sxs-lookup"><span data-stu-id="f439c-138">-Force</span></span>
<span data-ttu-id="f439c-139">表示此 Cmdlet 會覆寫現有的 blob。</span><span class="sxs-lookup"><span data-stu-id="f439c-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f439c-140">-InformationAction</span></span>
<span data-ttu-id="f439c-141">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="f439c-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f439c-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f439c-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f439c-143">持續</span><span class="sxs-lookup"><span data-stu-id="f439c-143">Continue</span></span>
- <span data-ttu-id="f439c-144">理會</span><span class="sxs-lookup"><span data-stu-id="f439c-144">Ignore</span></span>
- <span data-ttu-id="f439c-145">看</span><span class="sxs-lookup"><span data-stu-id="f439c-145">Inquire</span></span>
- <span data-ttu-id="f439c-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f439c-146">SilentlyContinue</span></span>
- <span data-ttu-id="f439c-147">停止</span><span class="sxs-lookup"><span data-stu-id="f439c-147">Stop</span></span>
- <span data-ttu-id="f439c-148">封存</span><span class="sxs-lookup"><span data-stu-id="f439c-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f439c-149">-InformationVariable</span></span>
<span data-ttu-id="f439c-150">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="f439c-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-151">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f439c-151">-Profile</span></span>
<span data-ttu-id="f439c-152">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f439c-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f439c-153">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f439c-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="f439c-154">-ReferenceName</span></span>
<span data-ttu-id="f439c-155">指定可用於參照延伸的使用者定義字串。</span><span class="sxs-lookup"><span data-stu-id="f439c-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="f439c-156">此參數是在第一次將延伸新增至虛擬機器時指定。</span><span class="sxs-lookup"><span data-stu-id="f439c-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="f439c-157">針對後續更新，您應該在更新副檔名時指定先前使用的參照名稱。</span><span class="sxs-lookup"><span data-stu-id="f439c-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="f439c-158">指派給延伸的 *ReferenceName* 會使用 **add-azurevm** Cmdlet 傳回。</span><span class="sxs-lookup"><span data-stu-id="f439c-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-159">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f439c-159">-StorageContext</span></span>
<span data-ttu-id="f439c-160">指定 Azure 儲存區內容，提供用來存取設定腳本的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="f439c-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="f439c-161">此內容提供對 *容器參數所* 指定之容器的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="f439c-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f439c-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="f439c-163">指定所有儲存服務的 DNS 端點尾碼，例如 "core.contoso.net"。</span><span class="sxs-lookup"><span data-stu-id="f439c-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-164">-版本</span><span class="sxs-lookup"><span data-stu-id="f439c-164">-Version</span></span>
<span data-ttu-id="f439c-165">指定要使用的 DSC 延伸的特定版本。</span><span class="sxs-lookup"><span data-stu-id="f439c-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="f439c-166">如果未指定此參數，則預設值會設定為 "1. \*"。</span><span class="sxs-lookup"><span data-stu-id="f439c-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-167">-VM</span><span class="sxs-lookup"><span data-stu-id="f439c-167">-VM</span></span>
<span data-ttu-id="f439c-168">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="f439c-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="f439c-169">-WmfVersion</span></span>
<span data-ttu-id="f439c-170">指定要在虛擬機器上安裝的 Windows Management Framework (WMF) 版本。</span><span class="sxs-lookup"><span data-stu-id="f439c-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="f439c-171">DSC 副檔名依賴于 WMF 更新中提供的 DSC 功能。</span><span class="sxs-lookup"><span data-stu-id="f439c-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="f439c-172">此參數指定要在虛擬機器上安裝的更新版本。</span><span class="sxs-lookup"><span data-stu-id="f439c-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="f439c-173">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f439c-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f439c-174">4.0。</span><span class="sxs-lookup"><span data-stu-id="f439c-174">4.0.</span></span>
<span data-ttu-id="f439c-175">安裝 WMF 4.0 （除非已安裝更新的版本）。</span><span class="sxs-lookup"><span data-stu-id="f439c-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="f439c-176">5.0。</span><span class="sxs-lookup"><span data-stu-id="f439c-176">5.0.</span></span>
<span data-ttu-id="f439c-177">安裝最新版本的 WMF 5.0。</span><span class="sxs-lookup"><span data-stu-id="f439c-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="f439c-178">最近.</span><span class="sxs-lookup"><span data-stu-id="f439c-178">latest.</span></span>
<span data-ttu-id="f439c-179">安裝最新的 WMF，目前是 WMF 5.0。</span><span class="sxs-lookup"><span data-stu-id="f439c-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="f439c-180">預設值為 [最新]。</span><span class="sxs-lookup"><span data-stu-id="f439c-180">The default value is latest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-181">-確認</span><span class="sxs-lookup"><span data-stu-id="f439c-181">-Confirm</span></span>
<span data-ttu-id="f439c-182">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f439c-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f439c-183">-WhatIf</span></span>
<span data-ttu-id="f439c-184">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f439c-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f439c-185">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f439c-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f439c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f439c-186">CommonParameters</span></span>
<span data-ttu-id="f439c-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f439c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f439c-188">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f439c-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f439c-189">輸入</span><span class="sxs-lookup"><span data-stu-id="f439c-189">INPUTS</span></span>

## <span data-ttu-id="f439c-190">輸出</span><span class="sxs-lookup"><span data-stu-id="f439c-190">OUTPUTS</span></span>

## <span data-ttu-id="f439c-191">筆記</span><span class="sxs-lookup"><span data-stu-id="f439c-191">NOTES</span></span>

## <span data-ttu-id="f439c-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="f439c-192">RELATED LINKS</span></span>

[<span data-ttu-id="f439c-193">AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f439c-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="f439c-194">移除-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f439c-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="f439c-195">移除-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f439c-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="f439c-196">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="f439c-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f439c-197">發佈-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f439c-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


