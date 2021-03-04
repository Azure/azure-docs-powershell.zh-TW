---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppSetting.md
ms.openlocfilehash: 5aff9382cbeac47c8d4423769d6256d34d5d109a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906190"
---
# <span data-ttu-id="b3073-101">Get-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="b3073-101">Get-AzFunctionAppSetting</span></span>

## <span data-ttu-id="b3073-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3073-102">SYNOPSIS</span></span>
<span data-ttu-id="b3073-103">為功能應用程式獲取應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-103">Gets app settings for a function app.</span></span>

## <span data-ttu-id="b3073-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3073-104">SYNTAX</span></span>

### <span data-ttu-id="b3073-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="b3073-105">ByName (Default)</span></span>
```
Get-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3073-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="b3073-106">ByObjectInput</span></span>
```
Get-AzFunctionAppSetting -InputObject <ISite> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b3073-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3073-107">DESCRIPTION</span></span>
<span data-ttu-id="b3073-108">為功能應用程式獲取應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-108">Gets app settings for a function app.</span></span>

## <span data-ttu-id="b3073-109">例子</span><span class="sxs-lookup"><span data-stu-id="b3073-109">EXAMPLES</span></span>

### <span data-ttu-id="b3073-110">範例 1：取得函數應用程式的 App 設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-110">Example 1: Get the app settings of a function app.</span></span>
```powershell
PS C:\> Get-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="b3073-111">此命令會獲得函數應用程式的 App 設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-111">This command gets the app settings of a function app.</span></span>

## <span data-ttu-id="b3073-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3073-112">PARAMETERS</span></span>

### <span data-ttu-id="b3073-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3073-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3073-114">-InputObject</span></span>
<span data-ttu-id="b3073-115">若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3073-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3073-116">-Name</span></span>
<span data-ttu-id="b3073-117">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-117">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3073-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3073-119">資源所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3073-119">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3073-120">-SubscriptionId</span></span>
<span data-ttu-id="b3073-121">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-121">The Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-122">-確認</span><span class="sxs-lookup"><span data-stu-id="b3073-122">-Confirm</span></span>
<span data-ttu-id="b3073-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3073-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3073-124">-WhatIf</span></span>
<span data-ttu-id="b3073-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3073-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3073-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3073-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3073-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3073-127">CommonParameters</span></span>
<span data-ttu-id="b3073-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3073-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3073-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3073-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3073-130">輸入</span><span class="sxs-lookup"><span data-stu-id="b3073-130">INPUTS</span></span>

### <span data-ttu-id="b3073-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="b3073-131">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="b3073-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b3073-132">OUTPUTS</span></span>

### <span data-ttu-id="b3073-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="b3073-133">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="b3073-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b3073-134">NOTES</span></span>

<span data-ttu-id="b3073-135">別名</span><span class="sxs-lookup"><span data-stu-id="b3073-135">ALIASES</span></span>

<span data-ttu-id="b3073-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b3073-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3073-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3073-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3073-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b3073-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3073-139">INPUTOBJECT： <ISite></span><span class="sxs-lookup"><span data-stu-id="b3073-139">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="b3073-140">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="b3073-140">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="b3073-141">`CloningInfoSourceWebAppId <String>`：來源應用程式的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-141">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="b3073-142">應用程式資源識別碼為適用于其他插槽的表單//訂閱/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，適用于其他插槽和/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}。</span><span class="sxs-lookup"><span data-stu-id="b3073-142">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="b3073-143">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-143">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="b3073-144">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="b3073-144">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b3073-145">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="b3073-145">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b3073-146">`[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 啟用用戶端關聯 <code>false</code> 性;停止傳送會話關聯 Cookie，此 Cookie 會在同一個會話中將用戶端要求路由至相同的實例。</span><span class="sxs-lookup"><span data-stu-id="b3073-146">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="b3073-147">預設值 <code>true</code> 為 。</span><span class="sxs-lookup"><span data-stu-id="b3073-147">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="b3073-148">`[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ;否則 <code>false</code> ，。</span><span class="sxs-lookup"><span data-stu-id="b3073-148">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="b3073-149">預設值 <code>false</code> 為 。</span><span class="sxs-lookup"><span data-stu-id="b3073-149">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-150">`[ClientCertExclusionPath <String>]`：用戶端憑證驗證逗號分隔排除路徑</span><span class="sxs-lookup"><span data-stu-id="b3073-150">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="b3073-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：複製的應用程式會優先于應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-151">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="b3073-152">如果指定，這些設定會優先于從來源應用程式複製的設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-152">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="b3073-153">否則，會保留來源應用程式的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-153">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="b3073-154">`[(Any) <String>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="b3073-154">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b3073-155">`[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 從來源應用程式複製自訂主機名稱;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-155">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-156">`[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 從來源應用程式複製原始程式碼管理;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-156">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 設定來源和目的地應用程式的負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b3073-157">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="b3073-158">`[CloningInfoCorrelationId <String>]`：複製作業的相關識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-158">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="b3073-159">此識別碼將多個複製作業系在一起，以使用相同的快照。</span><span class="sxs-lookup"><span data-stu-id="b3073-159">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="b3073-160">`[CloningInfoHostingEnvironment <String>]`：應用程式服務環境。</span><span class="sxs-lookup"><span data-stu-id="b3073-160">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="b3073-161">`[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 以覆寫目的地應用程式;否則 <code>false</code> ，。</span><span class="sxs-lookup"><span data-stu-id="b3073-161">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-162">`[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置，例如：美國西部或北歐洲</span><span class="sxs-lookup"><span data-stu-id="b3073-162">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="b3073-163">`[CloningInfoTrafficManagerProfileId <String>]`：要使用流量管理員設定檔的 ARM 資源識別碼 ，如果有。</span><span class="sxs-lookup"><span data-stu-id="b3073-163">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="b3073-164">流量管理員資源識別碼是表單 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。</span><span class="sxs-lookup"><span data-stu-id="b3073-164">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="b3073-165">`[CloningInfoTrafficManagerProfileName <String>]`：要建立的流量管理員設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-165">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="b3073-166">只有在流量管理員設定檔不存在時，才需要這項功能。</span><span class="sxs-lookup"><span data-stu-id="b3073-166">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="b3073-167">`[Config <ISiteConfig>]`：應用程式的組配置。</span><span class="sxs-lookup"><span data-stu-id="b3073-167">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="b3073-168">`IsPushEnabled <Boolean>`：套用或設定旗標，指出推入端點是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="b3073-168">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="b3073-169">`[ActionMinProcessExecutionTime <String>]`：執行動作前必須執行程式的最小時間</span><span class="sxs-lookup"><span data-stu-id="b3073-169">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="b3073-170">`[ActionType <AutoHealActionType?>]`：預先定義要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="b3073-170">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="b3073-171">`[AlwaysOn <Boolean?>]`： <code>true</code> 如果已啟用 Always On;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-171">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-172">`[ApiDefinitionUrl <String>]`：API 定義的 URL。</span><span class="sxs-lookup"><span data-stu-id="b3073-172">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="b3073-173">`[ApiManagementConfigId <String>]`：APIM-Api識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-173">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="b3073-174">`[AppCommandLine <String>]`：啟動 App 命令列。</span><span class="sxs-lookup"><span data-stu-id="b3073-174">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="b3073-175">`[AppSetting <INameValuePair[]>]`：應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="b3073-175">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="b3073-176">`[Name <String>]`：配對名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-176">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="b3073-177">`[Value <String>]`：配對值。</span><span class="sxs-lookup"><span data-stu-id="b3073-177">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="b3073-178">`[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動自動修復;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-178">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-179">`[AutoSwapSlotName <String>]`：自動交換插槽名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-179">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="b3073-180">`[ConnectionString <IConnStringInfo[]>]`：連接字串。</span><span class="sxs-lookup"><span data-stu-id="b3073-180">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="b3073-181">`[ConnectionString <String>]`：連接字串值。</span><span class="sxs-lookup"><span data-stu-id="b3073-181">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="b3073-182">`[Name <String>]`：連接字串的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-182">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="b3073-183">`[Type <ConnectionStringType?>]`：資料庫類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-183">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="b3073-184">`[CorAllowedOrigin <String[]>]`：獲取或設定應允許撥打跨來源電話的來源 (例如 http://example.com:12345) ：</span><span class="sxs-lookup"><span data-stu-id="b3073-184">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="b3073-185">使用 "\*" 允許所有專案。</span><span class="sxs-lookup"><span data-stu-id="b3073-185">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="b3073-186">`[CorSupportCredentials <Boolean?>]`：獲取或設定是否允許具有認證之 CORS 要求。</span><span class="sxs-lookup"><span data-stu-id="b3073-186">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="b3073-187">請參閱         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b3073-187">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="b3073-188">`[CustomActionExe <String>]`：執行可執行檔。</span><span class="sxs-lookup"><span data-stu-id="b3073-188">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="b3073-189">`[CustomActionParameter <String>]`：可執行檔的參數。</span><span class="sxs-lookup"><span data-stu-id="b3073-189">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="b3073-190">`[DefaultDocument <String[]>]`：預設檔。</span><span class="sxs-lookup"><span data-stu-id="b3073-190">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="b3073-191">`[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-191">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-192">`[DocumentRoot <String>]`：檔根目錄。</span><span class="sxs-lookup"><span data-stu-id="b3073-192">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="b3073-193">`[DynamicTagsJson <String>]`：獲取或設定包含動態標記清單的 JSON 字串，該清單會從推入註冊端點中的使用者聲明進行評估。</span><span class="sxs-lookup"><span data-stu-id="b3073-193">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="b3073-194">`[ExperimentRampUpRule <IRampUpRule[]>]`：快速上線規則清單。</span><span class="sxs-lookup"><span data-stu-id="b3073-194">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="b3073-195">`[ActionHostName <String>]`：位置的主機名稱，如果決定將流量重新導向到該位置。</span><span class="sxs-lookup"><span data-stu-id="b3073-195">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="b3073-196">例如</span><span class="sxs-lookup"><span data-stu-id="b3073-196">E.g.</span></span> <span data-ttu-id="b3073-197">myapp-stage.azurewebsites.net。</span><span class="sxs-lookup"><span data-stu-id="b3073-197">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="b3073-198">`[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站擴充功能中提供自訂決策演算法，以指定 URL。</span><span class="sxs-lookup"><span data-stu-id="b3073-198">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="b3073-199">請參閱基架和合約的 TiPCallback 網站擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b3073-199">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="b3073-200"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="b3073-200">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="b3073-201">`[ChangeIntervalInMinute <Int32?>]`：指定以分鐘為單位的間隔，以重新計算 ReroutePercentage。</span><span class="sxs-lookup"><span data-stu-id="b3073-201">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="b3073-202">`[ChangeStep <Double?>]`：在自動上手情況下，這是要新增/移除的步驟，直到到達 \n 或 <code>ReroutePercentage</code> <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-202">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="b3073-203">您可以在 TiPCallback 網站擴充功能中，以 .\nCustom 決策演算法指定的每 N 分鐘檢查網站 <code>ChangeIntervalInMinutes</code> 度量，URL 可以在其中指定 <code>ChangeDecisionCallbackUrl</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-203">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="b3073-204">`[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 會維持在下方的上限。</span><span class="sxs-lookup"><span data-stu-id="b3073-204">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="b3073-205">`[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 會維持在上方的下限。</span><span class="sxs-lookup"><span data-stu-id="b3073-205">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="b3073-206">`[Name <String>]`：路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-206">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="b3073-207">建議的名稱會指向在實驗中接收流量的插槽。</span><span class="sxs-lookup"><span data-stu-id="b3073-207">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="b3073-208">`[ReroutePercentage <Double?>]`：將會重新導向至的流量百分比 <code>ActionHostName</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-208">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="b3073-209">`[FtpsState <FtpsState?>]`：FTP /FTPS 服務的狀態</span><span class="sxs-lookup"><span data-stu-id="b3073-209">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="b3073-210">`[HandlerMapping <IHandlerMapping[]>]`：處理常式的映射。</span><span class="sxs-lookup"><span data-stu-id="b3073-210">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="b3073-211">`[Argument <String>]`：要傳遞到腳本處理器的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="b3073-211">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="b3073-212">`[Extension <String>]`：具有此副檔名的要求將會使用指定的 FastCGI 應用程式處理。</span><span class="sxs-lookup"><span data-stu-id="b3073-212">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="b3073-213">`[ScriptProcessor <String>]`：FastCGI 應用程式的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="b3073-213">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="b3073-214">`[HealthCheckPath <String>]`：健康狀態檢查路徑</span><span class="sxs-lookup"><span data-stu-id="b3073-214">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="b3073-215">`[Http20Enabled <Boolean?>]`：HTTP20Enabled：設定網站以允許用戶端以 HTTP2.0 進行連結</span><span class="sxs-lookup"><span data-stu-id="b3073-215">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="b3073-216">`[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-216">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="b3073-217">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="b3073-218">`[Action <String>]`：允許或拒絕此 IP 範圍的存取。</span><span class="sxs-lookup"><span data-stu-id="b3073-218">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="b3073-219">`[Description <String>]`：IP 限制規則描述。</span><span class="sxs-lookup"><span data-stu-id="b3073-219">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="b3073-220">`[IPAddress <String>]`：安全性限制的 IP 位址有效。</span><span class="sxs-lookup"><span data-stu-id="b3073-220">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="b3073-221">它可以是純粹 ipv4 位址 (子網路遮罩屬性) 或 CIDR 標記法 ，例如 ipv4/mask (前位比對) 。</span><span class="sxs-lookup"><span data-stu-id="b3073-221">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="b3073-222">對於 CIDR，不得指定子網路遮罩屬性。</span><span class="sxs-lookup"><span data-stu-id="b3073-222">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="b3073-223">`[Name <String>]`：IP 限制規則名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-223">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="b3073-224">`[Priority <Int32?>]`：IP 限制規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="b3073-224">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="b3073-225">`[SubnetMask <String>]`：限制有效之 IP 位址範圍的子網屏蔽。</span><span class="sxs-lookup"><span data-stu-id="b3073-225">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="b3073-226">`[SubnetTrafficTag <Int32?>]`： (子網) 標記</span><span class="sxs-lookup"><span data-stu-id="b3073-226">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="b3073-227">`[Tag <IPFilterTag?>]`：定義此 IP 篩選的用用方式。</span><span class="sxs-lookup"><span data-stu-id="b3073-227">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="b3073-228">這是為了支援對代理程式進行 IP 篩選。</span><span class="sxs-lookup"><span data-stu-id="b3073-228">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="b3073-229">`[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b3073-229">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="b3073-230">`[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記</span><span class="sxs-lookup"><span data-stu-id="b3073-230">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="b3073-231">`[JavaContainer <String>]`：JAVA 容器。</span><span class="sxs-lookup"><span data-stu-id="b3073-231">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="b3073-232">`[JavaContainerVersion <String>]`：JAVA 容器版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-232">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="b3073-233">`[JavaVersion <String>]`：JAVA 版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-233">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="b3073-234">`[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小使用量上限 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="b3073-234">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="b3073-235">`[LimitMaxMemoryInMb <Int64?>]`：允許記憶體使用量上限 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="b3073-235">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="b3073-236">`[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量百分比上限。</span><span class="sxs-lookup"><span data-stu-id="b3073-236">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="b3073-237">`[LinuxFxVersion <String>]`：Linux App 架構及版本</span><span class="sxs-lookup"><span data-stu-id="b3073-237">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="b3073-238">`[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。</span><span class="sxs-lookup"><span data-stu-id="b3073-238">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="b3073-239">`[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 啟用本地 MySQL;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-239">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-240">`[LogsDirectorySizeLimit <Int32?>]`：HTTP 記錄目錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="b3073-240">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="b3073-241">`[MachineKeyDecryption <String>]`：用於解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="b3073-241">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="b3073-242">`[MachineKeyDecryptionKey <String>]`：解密金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3073-242">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="b3073-243">`[MachineKeyValidation <String>]`：MachineKey 驗證。</span><span class="sxs-lookup"><span data-stu-id="b3073-243">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="b3073-244">`[MachineKeyValidationKey <String>]`：驗證鍵。</span><span class="sxs-lookup"><span data-stu-id="b3073-244">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="b3073-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。</span><span class="sxs-lookup"><span data-stu-id="b3073-245">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="b3073-246">`[ManagedServiceIdentityId <Int32?>]`：Managed Service Identity Id</span><span class="sxs-lookup"><span data-stu-id="b3073-246">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="b3073-247">`[MinTlsVersion <SupportedTlsVersions?>]`：MinTlsVersion：設定 SSL 要求所需的 TLS 最低版本</span><span class="sxs-lookup"><span data-stu-id="b3073-247">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="b3073-248">`[NetFrameworkVersion <String>]`：.NET Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-248">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="b3073-249">`[NodeVersion <String>]`：版本Node.js。</span><span class="sxs-lookup"><span data-stu-id="b3073-249">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="b3073-250">`[NumberOfWorker <Int32?>]`：員工人數。</span><span class="sxs-lookup"><span data-stu-id="b3073-250">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="b3073-251">`[PhpVersion <String>]`：PHP 版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-251">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="b3073-252">`[PowerShellVersion <String>]`：PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-252">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="b3073-253">`[PreWarmedInstanceCount <Int32?>]`：預先警告的實例數目。</span><span class="sxs-lookup"><span data-stu-id="b3073-253">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="b3073-254">此設定僅適用于消費和消費計畫</span><span class="sxs-lookup"><span data-stu-id="b3073-254">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="b3073-255">`[PublishingUsername <String>]`：發佈使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-255">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="b3073-256">`[PushKind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-256">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="b3073-257">`[PythonVersion <String>]`：版本為Python。</span><span class="sxs-lookup"><span data-stu-id="b3073-257">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="b3073-258">`[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端問題，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-258">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-259">`[RemoteDebuggingVersion <String>]`：遠端測試版本。</span><span class="sxs-lookup"><span data-stu-id="b3073-259">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="b3073-260">`[RequestCount <Int32?>]`：要求計數。</span><span class="sxs-lookup"><span data-stu-id="b3073-260">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="b3073-261">`[RequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="b3073-261">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="b3073-262">`[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤;否則 <code>false</code> ，。</span><span class="sxs-lookup"><span data-stu-id="b3073-262">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-263">`[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期日。</span><span class="sxs-lookup"><span data-stu-id="b3073-263">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="b3073-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：scm 的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="b3073-264">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="b3073-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：scm 使用主要之 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="b3073-265">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="b3073-266">`[ScmType <ScmType?>]`：SCM 類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-266">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="b3073-267">`[SlowRequestCount <Int32?>]`：要求計數。</span><span class="sxs-lookup"><span data-stu-id="b3073-267">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="b3073-268">`[SlowRequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="b3073-268">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="b3073-269">`[SlowRequestTimeTaken <String>]`：需要一些時間。</span><span class="sxs-lookup"><span data-stu-id="b3073-269">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="b3073-270">`[TagWhitelistJson <String>]`：獲取或設定 JSON 字串，其中包含由推入註冊端點使用之白名單的標記清單。</span><span class="sxs-lookup"><span data-stu-id="b3073-270">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="b3073-271">`[TagsRequiringAuth <String>]`：獲取或設定 JSON 字串，其中包含要求在推入註冊端點使用使用者驗證的標記清單。</span><span class="sxs-lookup"><span data-stu-id="b3073-271">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="b3073-272">標記可以包含字母數位字元，而下列字元：'_'、'@'、'#'、'.'、'：'、'-'。</span><span class="sxs-lookup"><span data-stu-id="b3073-272">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="b3073-273">驗證應在 PushRequestHandler 執行。</span><span class="sxs-lookup"><span data-stu-id="b3073-273">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="b3073-274">`[TracingOption <String>]`：追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="b3073-274">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="b3073-275">`[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="b3073-275">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="b3073-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="b3073-276">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="b3073-277">`[Count <Int32?>]`：要求計數。</span><span class="sxs-lookup"><span data-stu-id="b3073-277">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="b3073-278">`[Status <Int32?>]`：HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-278">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="b3073-279">`[SubStatus <Int32?>]`：要求子狀態。</span><span class="sxs-lookup"><span data-stu-id="b3073-279">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="b3073-280">`[TimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="b3073-280">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="b3073-281">`[Win32Status <Int32?>]`：Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-281">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="b3073-282">`[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 使用 32 位員工程式;否則 <code>false</code> ，。</span><span class="sxs-lookup"><span data-stu-id="b3073-282">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-283">`[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。</span><span class="sxs-lookup"><span data-stu-id="b3073-283">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="b3073-284">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="b3073-284">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="b3073-285">`[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預先載入;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-285">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="b3073-286">`[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="b3073-286">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="b3073-287">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="b3073-287">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="b3073-288">`[VirtualPath <String>]`：虛擬應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3073-288">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="b3073-289">`[VirtualPath <String>]`：虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="b3073-289">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="b3073-290">`[VnetName <String>]`：虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-290">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="b3073-291">`[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果啟用 WebSocket;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-291">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="b3073-292">`[WindowsFxVersion <String>]`：Xenon App Framework 與版本</span><span class="sxs-lookup"><span data-stu-id="b3073-292">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="b3073-293">`[XManagedServiceIdentityId <Int32?>]`：明確 Managed Service 身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="b3073-293">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="b3073-294">`[ContainerSize <Int32?>]`：函數容器的大小。</span><span class="sxs-lookup"><span data-stu-id="b3073-294">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="b3073-295">`[DailyMemoryTimeQuota <Int32?>]`：僅適用于動態應用程式 (允許的最大每日記憶體配額) 。</span><span class="sxs-lookup"><span data-stu-id="b3073-295">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="b3073-296">`[Enabled <Boolean?>]`： <code>true</code> 如果應用程式已啟用;否則 <code>false</code> ，.</span><span class="sxs-lookup"><span data-stu-id="b3073-296">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="b3073-297">將此值設定為 False 會停用應用程式 (應用程式離線) 。</span><span class="sxs-lookup"><span data-stu-id="b3073-297">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="b3073-298">`[HostNameSslState <IHostNameSslState[]>]`：Hostname SSL 狀態用來管理應用程式主機名稱的 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="b3073-298">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="b3073-299">`[HostType <HostType?>]`：表示 hostname 是標準或存放庫主機名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-299">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="b3073-300">`[Name <String>]`：Hostname。</span><span class="sxs-lookup"><span data-stu-id="b3073-300">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="b3073-301">`[SslState <SslState?>]`：SSL 類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-301">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="b3073-302">`[Thumbprint <String>]`：SSL 憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="b3073-302">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="b3073-303">`[ToUpdate <Boolean?>]`：設定 <code>true</code> 為更新現有的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="b3073-303">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="b3073-304">`[VirtualIP <String>]`：如果已啟用 IP 型 SSL，則指派給主機名稱的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b3073-304">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="b3073-305">`[HostNamesDisabled <Boolean?>]`： <code>true</code> 停用應用程式的公用主機名稱;否則 <code>false</code> ，。</span><span class="sxs-lookup"><span data-stu-id="b3073-305">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="b3073-306">如果 <code>true</code> ，應用程式只能透過 API 管理程式進行。</span><span class="sxs-lookup"><span data-stu-id="b3073-306">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="b3073-307">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3073-307">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="b3073-308">`[HttpsOnly <Boolean?>]`：HTTPsOnly：將網站設定為僅接受 HTTPs 要求。</span><span class="sxs-lookup"><span data-stu-id="b3073-308">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="b3073-309">Http 要求重新導向的問題</span><span class="sxs-lookup"><span data-stu-id="b3073-309">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="b3073-310">`[HyperV <Boolean?>]`：Hyper-V 沙箱。</span><span class="sxs-lookup"><span data-stu-id="b3073-310">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="b3073-311">`[IdentityType <ManagedServiceIdentityType?>]`：受管理服務身分識別的類型。</span><span class="sxs-lookup"><span data-stu-id="b3073-311">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="b3073-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：已指派與資源關聯的使用者身分清單。</span><span class="sxs-lookup"><span data-stu-id="b3073-312">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="b3073-313">使用者身分識別字典金鑰參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="b3073-313">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="b3073-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示任何屬性都可以新增到這個物件。</span><span class="sxs-lookup"><span data-stu-id="b3073-314">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b3073-315">`[IsXenon <Boolean?>]`：過時：Hyper-V 沙箱。</span><span class="sxs-lookup"><span data-stu-id="b3073-315">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="b3073-316">`[RedundancyMode <RedundancyMode?>]`：網站冗余模式</span><span class="sxs-lookup"><span data-stu-id="b3073-316">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="b3073-317">`[Reserved <Boolean?>]`： <code>true</code> 如果保留，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-317">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-318">`[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 在應用程式停止 (時) KUDU 或網站中停止 SCM;否則， <code>false</code></span><span class="sxs-lookup"><span data-stu-id="b3073-318">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="b3073-319">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="b3073-319">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="b3073-320">`[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為：「/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。</span><span class="sxs-lookup"><span data-stu-id="b3073-320">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="b3073-321">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3073-321">RELATED LINKS</span></span>

