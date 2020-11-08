---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136861"
---
# <span data-ttu-id="24ba6-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="24ba6-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="24ba6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="24ba6-103">重新開機函數 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-103">Restarts a function app.</span></span>

## <span data-ttu-id="24ba6-104">句法</span><span class="sxs-lookup"><span data-stu-id="24ba6-104">SYNTAX</span></span>

### <span data-ttu-id="24ba6-105">RestartByName (預設) </span><span class="sxs-lookup"><span data-stu-id="24ba6-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24ba6-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="24ba6-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24ba6-107">說明</span><span class="sxs-lookup"><span data-stu-id="24ba6-107">DESCRIPTION</span></span>
<span data-ttu-id="24ba6-108">重新開機函數 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-108">Restarts a function app.</span></span>

## <span data-ttu-id="24ba6-109">示例</span><span class="sxs-lookup"><span data-stu-id="24ba6-109">EXAMPLES</span></span>

### <span data-ttu-id="24ba6-110">範例1：透過名稱取得並重新啟動函數 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="24ba6-111">這個命令會透過名稱取得函數 app 並重新啟動。</span><span class="sxs-lookup"><span data-stu-id="24ba6-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="24ba6-112">範例2：依名稱重新開機函數 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="24ba6-113">這個命令會依名稱重新開機函數 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="24ba6-114">參數</span><span class="sxs-lookup"><span data-stu-id="24ba6-114">PARAMETERS</span></span>

### <span data-ttu-id="24ba6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ba6-115">-DefaultProfile</span></span>
<span data-ttu-id="24ba6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24ba6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="24ba6-117">-Force</span></span>
<span data-ttu-id="24ba6-118">強制 Cmdlet 重新開機函式應用程式，而不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="24ba6-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ba6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24ba6-119">-InputObject</span></span>
<span data-ttu-id="24ba6-120">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="24ba6-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24ba6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="24ba6-121">-Name</span></span>
<span data-ttu-id="24ba6-122">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ba6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24ba6-123">-PassThru</span></span>
<span data-ttu-id="24ba6-124">當命令成功時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="24ba6-124">Returns true when the command succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ba6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ba6-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ba6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24ba6-126">-SubscriptionId</span></span>
<span data-ttu-id="24ba6-127">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="24ba6-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ba6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="24ba6-128">-Confirm</span></span>
<span data-ttu-id="24ba6-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24ba6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24ba6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ba6-130">-WhatIf</span></span>
<span data-ttu-id="24ba6-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24ba6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ba6-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24ba6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24ba6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ba6-133">CommonParameters</span></span>
<span data-ttu-id="24ba6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24ba6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ba6-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="24ba6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ba6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="24ba6-136">INPUTS</span></span>

### <span data-ttu-id="24ba6-137">ISite 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="24ba6-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="24ba6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="24ba6-138">OUTPUTS</span></span>

### <span data-ttu-id="24ba6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="24ba6-139">System.Boolean</span></span>

## <span data-ttu-id="24ba6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="24ba6-140">NOTES</span></span>

<span data-ttu-id="24ba6-141">別名</span><span class="sxs-lookup"><span data-stu-id="24ba6-141">ALIASES</span></span>

<span data-ttu-id="24ba6-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="24ba6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24ba6-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="24ba6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24ba6-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="24ba6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24ba6-145">INPUTOBJECT <ISite> ：</span><span class="sxs-lookup"><span data-stu-id="24ba6-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="24ba6-146">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="24ba6-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="24ba6-147">`CloningInfoSourceWebAppId <String>`：源 app 的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24ba6-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="24ba6-148">App 資源識別碼的形式是生產槽的表單/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，而其他槽的/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} 則是。</span><span class="sxs-lookup"><span data-stu-id="24ba6-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="24ba6-149">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="24ba6-150">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="24ba6-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="24ba6-151">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="24ba6-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="24ba6-152">`[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 若要啟用客戶關係 <code>false</code> ，請停止傳送會話相關性 cookie，該 cookie 會將同一個會話中的用戶端要求路由至同一個實例。</span><span class="sxs-lookup"><span data-stu-id="24ba6-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="24ba6-153">預設值為 <code>true</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="24ba6-154">`[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="24ba6-155">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-156">`[ClientCertExclusionPath <String>]`：用戶端憑證驗證以逗號分隔的排除路徑</span><span class="sxs-lookup"><span data-stu-id="24ba6-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="24ba6-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：適用于克隆之 app 的應用程式設定覆寫。</span><span class="sxs-lookup"><span data-stu-id="24ba6-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="24ba6-158">如果已指定，這些設定會覆寫從源 app 克隆的設定。</span><span class="sxs-lookup"><span data-stu-id="24ba6-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="24ba6-159">否則，來源應用程式的應用程式設定會保留下來。</span><span class="sxs-lookup"><span data-stu-id="24ba6-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="24ba6-160">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="24ba6-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="24ba6-161">`[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 若要從來源 app 克隆自訂主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-162">`[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 若要從來源應用程式克隆來源控制，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 為來源和目的地 app 設定負載平衡。</span><span class="sxs-lookup"><span data-stu-id="24ba6-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="24ba6-164">`[CloningInfoCorrelationId <String>]`：克隆作業的相關 ID。</span><span class="sxs-lookup"><span data-stu-id="24ba6-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="24ba6-165">這個識別碼將多個克隆作業結合在一起，以使用相同的快照。</span><span class="sxs-lookup"><span data-stu-id="24ba6-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="24ba6-166">`[CloningInfoHostingEnvironment <String>]`： App 服務環境。</span><span class="sxs-lookup"><span data-stu-id="24ba6-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="24ba6-167">`[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 要覆寫目的地 app; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-168">`[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置（例如：西美國或北歐）</span><span class="sxs-lookup"><span data-stu-id="24ba6-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="24ba6-169">`[CloningInfoTrafficManagerProfileId <String>]`：要使用之流量管理器設定檔的 ARM 資源識別碼（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="24ba6-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="24ba6-170">流量管理員資源識別碼的形式為/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。</span><span class="sxs-lookup"><span data-stu-id="24ba6-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="24ba6-171">`[CloningInfoTrafficManagerProfileName <String>]`：要建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="24ba6-172">只有流量管理器設定檔尚不存在時，才需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="24ba6-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="24ba6-173">`[Config <ISiteConfig>]`：應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="24ba6-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="24ba6-174">`IsPushEnabled <Boolean>`：取得或設定指示是否已啟用推播端點的標誌。</span><span class="sxs-lookup"><span data-stu-id="24ba6-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="24ba6-175">`[ActionMinProcessExecutionTime <String>]`：在採取動作前必須執行的最短時間。</span><span class="sxs-lookup"><span data-stu-id="24ba6-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="24ba6-176">`[ActionType <AutoHealActionType?>]`：預先定義的要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="24ba6-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="24ba6-177">`[AlwaysOn <Boolean?>]`： <code>true</code> 如果啟用 [永不開啟]，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-178">`[ApiDefinitionUrl <String>]`： API 定義的 URL。</span><span class="sxs-lookup"><span data-stu-id="24ba6-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="24ba6-179">`[ApiManagementConfigId <String>]`： APIM-Api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="24ba6-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="24ba6-180">`[AppCommandLine <String>]`：啟動 App 命令列。</span><span class="sxs-lookup"><span data-stu-id="24ba6-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="24ba6-181">`[AppSetting <INameValuePair[]>]`：應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="24ba6-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="24ba6-182">`[Name <String>]`：配對名。</span><span class="sxs-lookup"><span data-stu-id="24ba6-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="24ba6-183">`[Value <String>]`： [配對] 值。</span><span class="sxs-lookup"><span data-stu-id="24ba6-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="24ba6-184">`[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動修復，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-185">`[AutoSwapSlotName <String>]`：自動交換槽名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="24ba6-186">`[ConnectionString <IConnStringInfo[]>]`：連接字串。</span><span class="sxs-lookup"><span data-stu-id="24ba6-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="24ba6-187">`[ConnectionString <String>]`：連接字串值。</span><span class="sxs-lookup"><span data-stu-id="24ba6-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="24ba6-188">`[Name <String>]`：連接字串的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="24ba6-189">`[Type <ConnectionStringType?>]`：資料庫的類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="24ba6-190">`[CorAllowedOrigin <String[]>]`：取得或設定允許進行交叉起源撥打電話的來源清單 (例如： http://example.com:12345) 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="24ba6-191">使用 "\*" 全部允許。</span><span class="sxs-lookup"><span data-stu-id="24ba6-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="24ba6-192">`[CorSupportCredentials <Boolean?>]`：取得或設定是否允許含身分驗證的 CORS 要求。</span><span class="sxs-lookup"><span data-stu-id="24ba6-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="24ba6-193">如需詳細         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="24ba6-194">`[CustomActionExe <String>]`：要執行的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="24ba6-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="24ba6-195">`[CustomActionParameter <String>]`：可執行檔的參數。</span><span class="sxs-lookup"><span data-stu-id="24ba6-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="24ba6-196">`[DefaultDocument <String[]>]`：預設檔。</span><span class="sxs-lookup"><span data-stu-id="24ba6-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="24ba6-197">`[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-198">`[DocumentRoot <String>]`：檔根。</span><span class="sxs-lookup"><span data-stu-id="24ba6-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="24ba6-199">`[DynamicTagsJson <String>]`：取得或設定一個 JSON 字串，其中包含將從推入註冊端點中的使用者宣告評估的動態標記清單。</span><span class="sxs-lookup"><span data-stu-id="24ba6-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="24ba6-200">`[ExperimentRampUpRule <IRampUpRule[]>]`：提升式規則清單。</span><span class="sxs-lookup"><span data-stu-id="24ba6-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="24ba6-201">`[ActionHostName <String>]`：如果決定要將流量重新導向到的槽主機名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="24ba6-202">例如.</span><span class="sxs-lookup"><span data-stu-id="24ba6-202">E.g.</span></span> <span data-ttu-id="24ba6-203">myapp-stage.azurewebsites.net。</span><span class="sxs-lookup"><span data-stu-id="24ba6-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="24ba6-204">`[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站副檔名中提供自訂決策演算法，您可以指定此 URL。</span><span class="sxs-lookup"><span data-stu-id="24ba6-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="24ba6-205">請參閱架設與合約的 TiPCallback 網站延伸。</span><span class="sxs-lookup"><span data-stu-id="24ba6-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="24ba6-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="24ba6-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="24ba6-207">`[ChangeIntervalInMinute <Int32?>]`：指定要重新評估 ReroutePercentage 的間隔時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="24ba6-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="24ba6-208">`[ChangeStep <Double?>]`：在自動向上斜坡案例中，這是要新增/移除的步驟， <code>ReroutePercentage</code> 直到到達 \n <code>MinReroutePercentage</code> 或         <code>MaxReroutePercentage</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="24ba6-209">在 .\NCustom 決策演算法中指定的每 N 分鐘數，都 <code>ChangeIntervalInMinutes</code> 可以在 TiPCallback 網站副檔名中提供，您可以在其中指定 URL <code>ChangeDecisionCallbackUrl</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="24ba6-210">`[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的上限。</span><span class="sxs-lookup"><span data-stu-id="24ba6-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="24ba6-211">`[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的較低邊界。</span><span class="sxs-lookup"><span data-stu-id="24ba6-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="24ba6-212">`[Name <String>]`：路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="24ba6-213">建議的名稱是指向將在實驗中接收流量的槽。</span><span class="sxs-lookup"><span data-stu-id="24ba6-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="24ba6-214">`[ReroutePercentage <Double?>]`：將會重新導向之流量的百分比 <code>ActionHostName</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="24ba6-215">`[FtpsState <FtpsState?>]`： FTP/FTPS 服務的狀態</span><span class="sxs-lookup"><span data-stu-id="24ba6-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="24ba6-216">`[HandlerMapping <IHandlerMapping[]>]`：處理常式對應。</span><span class="sxs-lookup"><span data-stu-id="24ba6-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="24ba6-217">`[Argument <String>]`：要傳送至腳本處理器的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="24ba6-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="24ba6-218">`[Extension <String>]`：具有此延伸的要求將會使用指定的 FastCGI 應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="24ba6-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="24ba6-219">`[ScriptProcessor <String>]`： FastCGI 應用程式的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="24ba6-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="24ba6-220">`[HealthCheckPath <String>]`：健康情況檢查路徑</span><span class="sxs-lookup"><span data-stu-id="24ba6-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="24ba6-221">`[Http20Enabled <Boolean?>]`： Http20Enabled：將網站設定為允許用戶端經由 HTTP 2.0 連線</span><span class="sxs-lookup"><span data-stu-id="24ba6-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="24ba6-222">`[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="24ba6-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="24ba6-224">`[Action <String>]`：允許或拒絕此 IP 範圍的存取權。</span><span class="sxs-lookup"><span data-stu-id="24ba6-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="24ba6-225">`[Description <String>]`： IP 限制規則描述。</span><span class="sxs-lookup"><span data-stu-id="24ba6-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="24ba6-226">`[IPAddress <String>]`： [安全性限制] 適用的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="24ba6-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="24ba6-227">它可以是純 ipv4 位址的形式 (必要的 SubnetMask 屬性) 或 CIDR 符號（例如 ipv4/遮罩 (前導位相符）) 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="24ba6-228">若是 CIDR，則不得指定 SubnetMask 屬性。</span><span class="sxs-lookup"><span data-stu-id="24ba6-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="24ba6-229">`[Name <String>]`： IP 限制規則名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="24ba6-230">`[Priority <Int32?>]`： IP 限制規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="24ba6-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="24ba6-231">`[SubnetMask <String>]`：限制有效的 IP 位址範圍的子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="24ba6-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="24ba6-232">`[SubnetTrafficTag <Int32?>]`： (內部) 子網流量標記</span><span class="sxs-lookup"><span data-stu-id="24ba6-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="24ba6-233">`[Tag <IPFilterTag?>]`：定義此 IP 篩選將用於何種用途。</span><span class="sxs-lookup"><span data-stu-id="24ba6-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="24ba6-234">這是為了支援在 proxy 上進行 IP 篩選。</span><span class="sxs-lookup"><span data-stu-id="24ba6-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="24ba6-235">`[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼</span><span class="sxs-lookup"><span data-stu-id="24ba6-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="24ba6-236">`[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記</span><span class="sxs-lookup"><span data-stu-id="24ba6-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="24ba6-237">`[JavaContainer <String>]`： JAVA 容器。</span><span class="sxs-lookup"><span data-stu-id="24ba6-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="24ba6-238">`[JavaContainerVersion <String>]`： JAVA 容器版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="24ba6-239">`[JavaVersion <String>]`： JAVA 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="24ba6-240">`[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小上限，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="24ba6-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="24ba6-241">`[LimitMaxMemoryInMb <Int64?>]`：允許的最大記憶體使用量（MB）。</span><span class="sxs-lookup"><span data-stu-id="24ba6-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="24ba6-242">`[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量上限百分比。</span><span class="sxs-lookup"><span data-stu-id="24ba6-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="24ba6-243">`[LinuxFxVersion <String>]`： Linux App 架構與版本</span><span class="sxs-lookup"><span data-stu-id="24ba6-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="24ba6-244">`[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。</span><span class="sxs-lookup"><span data-stu-id="24ba6-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="24ba6-245">`[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 若要啟用本機 MySQL，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-246">`[LogsDirectorySizeLimit <Int32?>]`： HTTP 記錄目錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="24ba6-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="24ba6-247">`[MachineKeyDecryption <String>]`：用於解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="24ba6-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="24ba6-248">`[MachineKeyDecryptionKey <String>]`：解密金鑰。</span><span class="sxs-lookup"><span data-stu-id="24ba6-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="24ba6-249">`[MachineKeyValidation <String>]`： MachineKey 驗證。</span><span class="sxs-lookup"><span data-stu-id="24ba6-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="24ba6-250">`[MachineKeyValidationKey <String>]`：驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="24ba6-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="24ba6-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。</span><span class="sxs-lookup"><span data-stu-id="24ba6-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="24ba6-252">`[ManagedServiceIdentityId <Int32?>]`：受管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="24ba6-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="24ba6-253">`[MinTlsVersion <SupportedTlsVersions?>]`： MinTlsVersion：設定 SSL 要求所需的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="24ba6-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="24ba6-254">`[NetFrameworkVersion <String>]`： .NET Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="24ba6-255">`[NodeVersion <String>]`： Node.js 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="24ba6-256">`[NumberOfWorker <Int32?>]`：工人的人數。</span><span class="sxs-lookup"><span data-stu-id="24ba6-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="24ba6-257">`[PhpVersion <String>]`： PHP 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="24ba6-258">`[PowerShellVersion <String>]`： PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="24ba6-259">`[PreWarmedInstanceCount <Int32?>]`： PreWarmed 實例數。</span><span class="sxs-lookup"><span data-stu-id="24ba6-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="24ba6-260">此設定僅適用于消耗量與彈性方案</span><span class="sxs-lookup"><span data-stu-id="24ba6-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="24ba6-261">`[PublishingUsername <String>]`：發佈使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="24ba6-262">`[PushKind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="24ba6-263">`[PythonVersion <String>]`： Python 版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="24ba6-264">`[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端偵錯，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-265">`[RemoteDebuggingVersion <String>]`：遠端偵錯版本。</span><span class="sxs-lookup"><span data-stu-id="24ba6-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="24ba6-266">`[RequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="24ba6-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="24ba6-267">`[RequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="24ba6-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="24ba6-268">`[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-269">`[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期時間。</span><span class="sxs-lookup"><span data-stu-id="24ba6-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="24ba6-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：適用于 scm 的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="24ba6-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="24ba6-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：適用于 scm 的 IP 安全性限制使用 main。</span><span class="sxs-lookup"><span data-stu-id="24ba6-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="24ba6-272">`[ScmType <ScmType?>]`： SCM 類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="24ba6-273">`[SlowRequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="24ba6-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="24ba6-274">`[SlowRequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="24ba6-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="24ba6-275">`[SlowRequestTimeTaken <String>]`：拍攝的時間。</span><span class="sxs-lookup"><span data-stu-id="24ba6-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="24ba6-276">`[TagWhitelistJson <String>]`：取得或設定一個 JSON 字串，其中包含由推入註冊端點所使用的白板標記清單。</span><span class="sxs-lookup"><span data-stu-id="24ba6-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="24ba6-277">`[TagsRequiringAuth <String>]`：取得或設定一個 JSON 字串，其中包含需要使用者驗證才能用於推入註冊端點的標記清單。</span><span class="sxs-lookup"><span data-stu-id="24ba6-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="24ba6-278">標記可以由字母數位字元及下列專案所組成：「_ '、' @ '、' # '、'. '、'： '、'-」。</span><span class="sxs-lookup"><span data-stu-id="24ba6-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="24ba6-279">驗證應該在 PushRequestHandler 進行。</span><span class="sxs-lookup"><span data-stu-id="24ba6-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="24ba6-280">`[TracingOption <String>]`：追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="24ba6-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="24ba6-281">`[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="24ba6-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="24ba6-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="24ba6-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="24ba6-283">`[Count <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="24ba6-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="24ba6-284">`[Status <Int32?>]`： HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="24ba6-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="24ba6-285">`[SubStatus <Int32?>]`：要求子狀態。</span><span class="sxs-lookup"><span data-stu-id="24ba6-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="24ba6-286">`[TimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="24ba6-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="24ba6-287">`[Win32Status <Int32?>]`： Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="24ba6-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="24ba6-288">`[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 若要使用32位的輔助進程，請按相反的方式 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-289">`[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。</span><span class="sxs-lookup"><span data-stu-id="24ba6-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="24ba6-290">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="24ba6-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="24ba6-291">`[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預載入，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="24ba6-292">`[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="24ba6-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="24ba6-293">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="24ba6-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="24ba6-294">`[VirtualPath <String>]`：虛擬應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="24ba6-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="24ba6-295">`[VirtualPath <String>]`：虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="24ba6-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="24ba6-296">`[VnetName <String>]`：虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="24ba6-297">`[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果已啟用 WebSocket，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="24ba6-298">`[WindowsFxVersion <String>]`： Xenon 應用程式架構與版本</span><span class="sxs-lookup"><span data-stu-id="24ba6-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="24ba6-299">`[XManagedServiceIdentityId <Int32?>]`：顯式管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="24ba6-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="24ba6-300">`[ContainerSize <Int32?>]`：函數容器的大小。</span><span class="sxs-lookup"><span data-stu-id="24ba6-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="24ba6-301">`[DailyMemoryTimeQuota <Int32?>]`： (僅適用于動態 app 的 [允許的每日記憶體時間配額限制]) 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="24ba6-302">`[Enabled <Boolean?>]`： <code>true</code> 如果已啟用應用程式，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="24ba6-303">將此值設定為 false 會停用 app (將 app 離線) 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="24ba6-304">`[HostNameSslState <IHostNameSslState[]>]`：主機名稱 SSL 狀態是用來管理 app 主機名稱的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="24ba6-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="24ba6-305">`[HostType <HostType?>]`：表示主機名稱是標準版還是知識庫主機名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="24ba6-306">`[Name <String>]`主機.</span><span class="sxs-lookup"><span data-stu-id="24ba6-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="24ba6-307">`[SslState <SslState?>]`： SSL 類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="24ba6-308">`[Thumbprint <String>]`： SSL 憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="24ba6-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="24ba6-309">`[ToUpdate <Boolean?>]`：設定為 <code>true</code> 以更新現有的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="24ba6-310">`[VirtualIP <String>]`：如果啟用 IP SSL，則會指派給主機名稱的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="24ba6-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="24ba6-311">`[HostNamesDisabled <Boolean?>]`： <code>true</code> 若要停用應用程式的公用主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="24ba6-312">如果 <code>true</code> 是，只能透過 API 管理程式存取 app。</span><span class="sxs-lookup"><span data-stu-id="24ba6-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="24ba6-313">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="24ba6-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="24ba6-314">`[HttpsOnly <Boolean?>]`： HttpsOnly：將網站配置為只接受 HTTPs 要求。</span><span class="sxs-lookup"><span data-stu-id="24ba6-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="24ba6-315">Http 要求的重新導向問題</span><span class="sxs-lookup"><span data-stu-id="24ba6-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="24ba6-316">`[HyperV <Boolean?>]`： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="24ba6-317">`[IdentityType <ManagedServiceIdentityType?>]`：受管理的服務身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="24ba6-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="24ba6-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：指派與資源相關聯之身分識別的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="24ba6-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="24ba6-319">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="24ba6-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="24ba6-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="24ba6-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="24ba6-321">`[IsXenon <Boolean?>]`：已過時： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="24ba6-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="24ba6-322">`[RedundancyMode <RedundancyMode?>]`：網站冗余模式</span><span class="sxs-lookup"><span data-stu-id="24ba6-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="24ba6-323">`[Reserved <Boolean?>]`： <code>true</code> 如果保留，則為，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-324">`[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 若要在應用程式停止時停止 SCM (KUDU) 網站，請按相反步驟操作 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="24ba6-325">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="24ba6-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="24ba6-326">`[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為： "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。</span><span class="sxs-lookup"><span data-stu-id="24ba6-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="24ba6-327">相關連結</span><span class="sxs-lookup"><span data-stu-id="24ba6-327">RELATED LINKS</span></span>

