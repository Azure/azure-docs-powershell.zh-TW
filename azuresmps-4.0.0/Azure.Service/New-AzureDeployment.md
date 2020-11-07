---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967375"
---
# <span data-ttu-id="948cf-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="948cf-101">New-AzureDeployment</span></span>

## <span data-ttu-id="948cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="948cf-102">SYNOPSIS</span></span>
<span data-ttu-id="948cf-103">從服務建立部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="948cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="948cf-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="948cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="948cf-105">DESCRIPTION</span></span>
<span data-ttu-id="948cf-106">**新的-AzureDeployment** Cmdlet 會從構成網頁角色和輔助角色的服務建立 Azure 部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="948cf-107">這個 Cmdlet 會根據套件檔案 () 與服務設定檔案 ( .cscfg) 建立部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="948cf-108">指定部署環境中唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="948cf-109">使用 **New-add-azurevm** Cmdlet，根據 Azure 虛擬機器建立部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="948cf-110">示例</span><span class="sxs-lookup"><span data-stu-id="948cf-110">EXAMPLES</span></span>

### <span data-ttu-id="948cf-111">範例1：建立部署</span><span class="sxs-lookup"><span data-stu-id="948cf-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="948cf-112">這個命令會根據名為 ContosoPackage 的套件，以及名為 ContosoConfiguration 的 cspkg 來建立生產部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="948cf-113">該命令會指定部署的標籤。</span><span class="sxs-lookup"><span data-stu-id="948cf-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="948cf-114">它不會指定名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-114">It does not specify a name.</span></span>
<span data-ttu-id="948cf-115">這個 Cmdlet 會建立 GUID 做為名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="948cf-116">範例2：根據延伸設定建立部署</span><span class="sxs-lookup"><span data-stu-id="948cf-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="948cf-117">這個命令會根據套件和設定建立生產部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="948cf-118">該命令會指定一個名為 ContosoExtensionConfig 的延伸設定。</span><span class="sxs-lookup"><span data-stu-id="948cf-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="948cf-119">這個 Cmdlet 會建立 Guid 做為名稱和標籤。</span><span class="sxs-lookup"><span data-stu-id="948cf-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="948cf-120">參數</span><span class="sxs-lookup"><span data-stu-id="948cf-120">PARAMETERS</span></span>

### <span data-ttu-id="948cf-121">-配置</span><span class="sxs-lookup"><span data-stu-id="948cf-121">-Configuration</span></span>
<span data-ttu-id="948cf-122">指定服務設定檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="948cf-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="948cf-123">-DoNotStart</span></span>
<span data-ttu-id="948cf-124">指定此 Cmdlet 不會啟動部署。</span><span class="sxs-lookup"><span data-stu-id="948cf-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="948cf-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="948cf-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="948cf-126">指定擴展設定物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="948cf-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="948cf-127">-InformationAction</span></span>
<span data-ttu-id="948cf-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="948cf-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="948cf-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="948cf-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="948cf-130">持續</span><span class="sxs-lookup"><span data-stu-id="948cf-130">Continue</span></span>
- <span data-ttu-id="948cf-131">理會</span><span class="sxs-lookup"><span data-stu-id="948cf-131">Ignore</span></span>
- <span data-ttu-id="948cf-132">看</span><span class="sxs-lookup"><span data-stu-id="948cf-132">Inquire</span></span>
- <span data-ttu-id="948cf-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="948cf-133">SilentlyContinue</span></span>
- <span data-ttu-id="948cf-134">停止</span><span class="sxs-lookup"><span data-stu-id="948cf-134">Stop</span></span>
- <span data-ttu-id="948cf-135">封存</span><span class="sxs-lookup"><span data-stu-id="948cf-135">Suspend</span></span>

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

### <span data-ttu-id="948cf-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="948cf-136">-InformationVariable</span></span>
<span data-ttu-id="948cf-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="948cf-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="948cf-138">-標籤</span><span class="sxs-lookup"><span data-stu-id="948cf-138">-Label</span></span>
<span data-ttu-id="948cf-139">指定部署的標籤名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="948cf-140">如果您沒有指定標籤，此 Cmdlet 會使用 GUID。</span><span class="sxs-lookup"><span data-stu-id="948cf-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="948cf-141">-Name</span></span>
<span data-ttu-id="948cf-142">指定部署名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-142">Specifies a deployment name.</span></span>
<span data-ttu-id="948cf-143">如果您沒有指定名稱，此 Cmdlet 會使用 GUID。</span><span class="sxs-lookup"><span data-stu-id="948cf-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-144">-套件</span><span class="sxs-lookup"><span data-stu-id="948cf-144">-Package</span></span>
<span data-ttu-id="948cf-145">在相同訂閱或專案內的儲存空間中指定 cspkg 檔案的路徑或 URI。</span><span class="sxs-lookup"><span data-stu-id="948cf-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-146">-設定檔</span><span class="sxs-lookup"><span data-stu-id="948cf-146">-Profile</span></span>
<span data-ttu-id="948cf-147">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="948cf-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="948cf-148">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="948cf-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="948cf-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="948cf-149">-ServiceName</span></span>
<span data-ttu-id="948cf-150">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="948cf-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-151">-槽</span><span class="sxs-lookup"><span data-stu-id="948cf-151">-Slot</span></span>
<span data-ttu-id="948cf-152">指定此 Cmdlet 建立部署的環境。</span><span class="sxs-lookup"><span data-stu-id="948cf-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="948cf-153">有效值為：暫存與生產。</span><span class="sxs-lookup"><span data-stu-id="948cf-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="948cf-154">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="948cf-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948cf-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="948cf-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="948cf-156">指定警告訊息是錯誤的。</span><span class="sxs-lookup"><span data-stu-id="948cf-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="948cf-157">如果您指定此參數，就會出現警告訊息，導致部署失敗。</span><span class="sxs-lookup"><span data-stu-id="948cf-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="948cf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948cf-158">CommonParameters</span></span>
<span data-ttu-id="948cf-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="948cf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948cf-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="948cf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948cf-161">輸入</span><span class="sxs-lookup"><span data-stu-id="948cf-161">INPUTS</span></span>

## <span data-ttu-id="948cf-162">輸出</span><span class="sxs-lookup"><span data-stu-id="948cf-162">OUTPUTS</span></span>

## <span data-ttu-id="948cf-163">筆記</span><span class="sxs-lookup"><span data-stu-id="948cf-163">NOTES</span></span>

## <span data-ttu-id="948cf-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="948cf-164">RELATED LINKS</span></span>

[<span data-ttu-id="948cf-165">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="948cf-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="948cf-166">AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="948cf-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="948cf-167">移動流覽 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="948cf-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="948cf-168">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="948cf-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="948cf-169">移除-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="948cf-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="948cf-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="948cf-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


