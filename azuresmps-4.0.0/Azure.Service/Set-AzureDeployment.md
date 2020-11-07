---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967510"
---
# <span data-ttu-id="8896e-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8896e-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="8896e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8896e-102">SYNOPSIS</span></span>
<span data-ttu-id="8896e-103">修改部署的狀態、配置設定或升級模式。</span><span class="sxs-lookup"><span data-stu-id="8896e-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="8896e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8896e-104">SYNTAX</span></span>

### <span data-ttu-id="8896e-105">更新</span><span class="sxs-lookup"><span data-stu-id="8896e-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8896e-106">設定</span><span class="sxs-lookup"><span data-stu-id="8896e-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8896e-107">狀態值</span><span class="sxs-lookup"><span data-stu-id="8896e-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8896e-108">說明</span><span class="sxs-lookup"><span data-stu-id="8896e-108">DESCRIPTION</span></span>
<span data-ttu-id="8896e-109">AzureDeployment Cmdlet 會修改 Azure 部署的狀態、 **設定** 設定或升級模式。</span><span class="sxs-lookup"><span data-stu-id="8896e-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="8896e-110">您可以將部署的狀態變更為 [執行] 或 [暫停]。</span><span class="sxs-lookup"><span data-stu-id="8896e-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="8896e-111">您可以變更部署的 .cscfg 檔案。</span><span class="sxs-lookup"><span data-stu-id="8896e-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="8896e-112">您可以設定升級模式並更新設定檔。</span><span class="sxs-lookup"><span data-stu-id="8896e-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="8896e-113">使用 **AzureWalkUpgradeDomain** Cmdlet 來啟動升級。</span><span class="sxs-lookup"><span data-stu-id="8896e-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="8896e-114">示例</span><span class="sxs-lookup"><span data-stu-id="8896e-114">EXAMPLES</span></span>

### <span data-ttu-id="8896e-115">範例1：變更部署的狀態</span><span class="sxs-lookup"><span data-stu-id="8896e-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="8896e-116">這個命令會將生產環境中名為 ContosoService 的服務的部署狀態設定為 [執行]。</span><span class="sxs-lookup"><span data-stu-id="8896e-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="8896e-117">範例2：指派其他設定檔至部署</span><span class="sxs-lookup"><span data-stu-id="8896e-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="8896e-118">這個命令會為暫存環境中名為 ContosoService 的服務的部署指派不同的配置檔案。</span><span class="sxs-lookup"><span data-stu-id="8896e-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="8896e-119">範例3：將升級模式設定為 [自動]</span><span class="sxs-lookup"><span data-stu-id="8896e-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="8896e-120">這個命令會將升級模式設定為 [自動]，並指定升級套件與新的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8896e-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="8896e-121">範例4：在服務中安裝延伸設定</span><span class="sxs-lookup"><span data-stu-id="8896e-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="8896e-122">這個命令會在指定的雲端服務中安裝擴充設定，並將其套用至角色。</span><span class="sxs-lookup"><span data-stu-id="8896e-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="8896e-123">參數</span><span class="sxs-lookup"><span data-stu-id="8896e-123">PARAMETERS</span></span>

### <span data-ttu-id="8896e-124">-Config</span><span class="sxs-lookup"><span data-stu-id="8896e-124">-Config</span></span>
<span data-ttu-id="8896e-125">指定此 Cmdlet 會修改部署的配置。</span><span class="sxs-lookup"><span data-stu-id="8896e-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-126">-配置</span><span class="sxs-lookup"><span data-stu-id="8896e-126">-Configuration</span></span>
<span data-ttu-id="8896e-127">指定 .cscfg 設定檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8896e-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="8896e-128">您可以指定升級或設定變更的設定檔。</span><span class="sxs-lookup"><span data-stu-id="8896e-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="8896e-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="8896e-130">指定擴展設定物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="8896e-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="8896e-131">-Force</span></span>
<span data-ttu-id="8896e-132">表示 Cmdlet 會執行強制升級。</span><span class="sxs-lookup"><span data-stu-id="8896e-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8896e-133">-InformationAction</span></span>
<span data-ttu-id="8896e-134">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8896e-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8896e-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8896e-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8896e-136">持續</span><span class="sxs-lookup"><span data-stu-id="8896e-136">Continue</span></span>
- <span data-ttu-id="8896e-137">理會</span><span class="sxs-lookup"><span data-stu-id="8896e-137">Ignore</span></span>
- <span data-ttu-id="8896e-138">看</span><span class="sxs-lookup"><span data-stu-id="8896e-138">Inquire</span></span>
- <span data-ttu-id="8896e-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8896e-139">SilentlyContinue</span></span>
- <span data-ttu-id="8896e-140">停止</span><span class="sxs-lookup"><span data-stu-id="8896e-140">Stop</span></span>
- <span data-ttu-id="8896e-141">封存</span><span class="sxs-lookup"><span data-stu-id="8896e-141">Suspend</span></span>

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

### <span data-ttu-id="8896e-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8896e-142">-InformationVariable</span></span>
<span data-ttu-id="8896e-143">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8896e-143">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8896e-144">-標籤</span><span class="sxs-lookup"><span data-stu-id="8896e-144">-Label</span></span>
<span data-ttu-id="8896e-145">指定升級部署的標籤。</span><span class="sxs-lookup"><span data-stu-id="8896e-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-146">模式</span><span class="sxs-lookup"><span data-stu-id="8896e-146">-Mode</span></span>
<span data-ttu-id="8896e-147">指定升級模式。</span><span class="sxs-lookup"><span data-stu-id="8896e-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="8896e-148">有效值為：</span><span class="sxs-lookup"><span data-stu-id="8896e-148">Valid values are:</span></span> 

- <span data-ttu-id="8896e-149">自動</span><span class="sxs-lookup"><span data-stu-id="8896e-149">Auto</span></span> 
- <span data-ttu-id="8896e-150">手動</span><span class="sxs-lookup"><span data-stu-id="8896e-150">Manual</span></span> 
- <span data-ttu-id="8896e-151">辦公</span><span class="sxs-lookup"><span data-stu-id="8896e-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="8896e-152">-NewStatus</span></span>
<span data-ttu-id="8896e-153">指定部署的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="8896e-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="8896e-154">有效值為： [正在執行] 和 [暫停]。</span><span class="sxs-lookup"><span data-stu-id="8896e-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-155">-套件</span><span class="sxs-lookup"><span data-stu-id="8896e-155">-Package</span></span>
<span data-ttu-id="8896e-156">指定升級套件檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8896e-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-157">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8896e-157">-Profile</span></span>
<span data-ttu-id="8896e-158">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8896e-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8896e-159">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8896e-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8896e-160">-擁有方</span><span class="sxs-lookup"><span data-stu-id="8896e-160">-RoleName</span></span>
<span data-ttu-id="8896e-161">指定要升級的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="8896e-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8896e-162">-ServiceName</span></span>
<span data-ttu-id="8896e-163">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8896e-163">Specifies the name of the Azure service of the deployment.</span></span>

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

### <span data-ttu-id="8896e-164">-槽</span><span class="sxs-lookup"><span data-stu-id="8896e-164">-Slot</span></span>
<span data-ttu-id="8896e-165">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="8896e-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="8896e-166">有效值為： [生產] 和 [轉移]。</span><span class="sxs-lookup"><span data-stu-id="8896e-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-167">-狀態</span><span class="sxs-lookup"><span data-stu-id="8896e-167">-Status</span></span>
<span data-ttu-id="8896e-168">指定此 Cmdlet 會變更部署的狀態。</span><span class="sxs-lookup"><span data-stu-id="8896e-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-169">-升級</span><span class="sxs-lookup"><span data-stu-id="8896e-169">-Upgrade</span></span>
<span data-ttu-id="8896e-170">指定此 Cmdlet 會升級部署。</span><span class="sxs-lookup"><span data-stu-id="8896e-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8896e-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8896e-171">CommonParameters</span></span>
<span data-ttu-id="8896e-172">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8896e-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8896e-173">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8896e-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8896e-174">輸入</span><span class="sxs-lookup"><span data-stu-id="8896e-174">INPUTS</span></span>

## <span data-ttu-id="8896e-175">輸出</span><span class="sxs-lookup"><span data-stu-id="8896e-175">OUTPUTS</span></span>

## <span data-ttu-id="8896e-176">筆記</span><span class="sxs-lookup"><span data-stu-id="8896e-176">NOTES</span></span>

## <span data-ttu-id="8896e-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="8896e-177">RELATED LINKS</span></span>

[<span data-ttu-id="8896e-178">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8896e-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="8896e-179">AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="8896e-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="8896e-180">移動流覽 AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8896e-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="8896e-181">新-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8896e-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="8896e-182">移除-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="8896e-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="8896e-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="8896e-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


