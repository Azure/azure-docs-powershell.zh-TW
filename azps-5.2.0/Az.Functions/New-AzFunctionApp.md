---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278667"
---
# <span data-ttu-id="8e52a-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="8e52a-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="8e52a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e52a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e52a-103">建立函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-103">Creates a function app.</span></span>

## <span data-ttu-id="8e52a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e52a-104">SYNTAX</span></span>

### <span data-ttu-id="8e52a-105">預設)  (消耗量</span><span class="sxs-lookup"><span data-stu-id="8e52a-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e52a-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e52a-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8e52a-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="8e52a-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8e52a-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e52a-108">DESCRIPTION</span></span>
<span data-ttu-id="8e52a-109">建立函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-109">Creates a function app.</span></span>

## <span data-ttu-id="8e52a-110">示例</span><span class="sxs-lookup"><span data-stu-id="8e52a-110">EXAMPLES</span></span>

### <span data-ttu-id="8e52a-111">範例1：在美國中部建立消耗量 PowerShell 函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="8e52a-112">這個命令會在美國中部建立消耗量 PowerShell 函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="8e52a-113">範例2：建立將託管在服務方案中的 PowerShell 函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="8e52a-114">這個命令會建立將託管在服務方案中的 PowerShell 函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="8e52a-115">範例3：使用私人 ACR 圖像建立函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="8e52a-116">這個命令會使用 [私人 ACR] 影像來建立函數 app。</span><span class="sxs-lookup"><span data-stu-id="8e52a-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="8e52a-117">參數</span><span class="sxs-lookup"><span data-stu-id="8e52a-117">PARAMETERS</span></span>

### <span data-ttu-id="8e52a-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="8e52a-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="8e52a-119">要新增之 App Insights 的檢測鍵。</span><span class="sxs-lookup"><span data-stu-id="8e52a-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="8e52a-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="8e52a-121">要新增至函數 App 之現有 App Insights 專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e52a-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="8e52a-122">-AppSetting</span></span>
<span data-ttu-id="8e52a-123">函數 app 設定。</span><span class="sxs-lookup"><span data-stu-id="8e52a-123">Function app settings.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e52a-124">-AsJob</span></span>
<span data-ttu-id="8e52a-125">將 Cmdlet 作為背景作業執行。</span><span class="sxs-lookup"><span data-stu-id="8e52a-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="8e52a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e52a-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="8e52a-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8e52a-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="8e52a-128">停用在建立函數 app 期間建立 application insights 資源。</span><span class="sxs-lookup"><span data-stu-id="8e52a-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="8e52a-129">沒有可用的記錄。</span><span class="sxs-lookup"><span data-stu-id="8e52a-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="8e52a-130">-DockerImageName</span></span>
<span data-ttu-id="8e52a-131">僅限 Linux。</span><span class="sxs-lookup"><span data-stu-id="8e52a-131">Linux only.</span></span>
<span data-ttu-id="8e52a-132">來自 Docker 登錄的容器影像名稱，例如 publisher/image name：標記。</span><span class="sxs-lookup"><span data-stu-id="8e52a-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="8e52a-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="8e52a-134">容器登錄的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="8e52a-134">The container registry user name and password.</span></span>
<span data-ttu-id="8e52a-135">私人機構所需。</span><span class="sxs-lookup"><span data-stu-id="8e52a-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="8e52a-136">-FunctionsVersion</span></span>
<span data-ttu-id="8e52a-137">函數版本。</span><span class="sxs-lookup"><span data-stu-id="8e52a-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="8e52a-138">-IdentityID</span></span>
<span data-ttu-id="8e52a-139">指定與函數 app 相關聯的使用者識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="8e52a-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="8e52a-140">使用者身分識別參照將是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} '</span><span class="sxs-lookup"><span data-stu-id="8e52a-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="8e52a-141">-IdentityType</span></span>
<span data-ttu-id="8e52a-142">指定用於函數 app 的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="8e52a-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="8e52a-143">此參數可接受的值為：-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="8e52a-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-144">-位置</span><span class="sxs-lookup"><span data-stu-id="8e52a-144">-Location</span></span>
<span data-ttu-id="8e52a-145">消耗量方案的位置。</span><span class="sxs-lookup"><span data-stu-id="8e52a-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e52a-146">-Name</span></span>
<span data-ttu-id="8e52a-147">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e52a-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8e52a-148">-NoWait</span></span>
<span data-ttu-id="8e52a-149">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="8e52a-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="8e52a-150">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="8e52a-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8e52a-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="8e52a-151">-OSType</span></span>
<span data-ttu-id="8e52a-152">主持函數 app 的 OS。</span><span class="sxs-lookup"><span data-stu-id="8e52a-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e52a-153">-PassThru</span></span>
<span data-ttu-id="8e52a-154">當命令成功時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="8e52a-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="8e52a-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="8e52a-155">-PlanName</span></span>
<span data-ttu-id="8e52a-156">服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e52a-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e52a-157">-ResourceGroupName</span></span>
<span data-ttu-id="8e52a-158">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e52a-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-159">-執行時間</span><span class="sxs-lookup"><span data-stu-id="8e52a-159">-Runtime</span></span>
<span data-ttu-id="8e52a-160">函數執行時間。</span><span class="sxs-lookup"><span data-stu-id="8e52a-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="8e52a-161">-RuntimeVersion</span></span>
<span data-ttu-id="8e52a-162">函數執行時間。</span><span class="sxs-lookup"><span data-stu-id="8e52a-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8e52a-163">-StorageAccountName</span></span>
<span data-ttu-id="8e52a-164">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e52a-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e52a-165">-SubscriptionId</span></span>
<span data-ttu-id="8e52a-166">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="8e52a-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e52a-167">-Tag</span></span>
<span data-ttu-id="8e52a-168">資源標記。</span><span class="sxs-lookup"><span data-stu-id="8e52a-168">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e52a-169">-確認</span><span class="sxs-lookup"><span data-stu-id="8e52a-169">-Confirm</span></span>
<span data-ttu-id="8e52a-170">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8e52a-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e52a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e52a-171">-WhatIf</span></span>
<span data-ttu-id="8e52a-172">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e52a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e52a-173">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e52a-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e52a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e52a-174">CommonParameters</span></span>
<span data-ttu-id="8e52a-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e52a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e52a-176">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e52a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e52a-177">輸入</span><span class="sxs-lookup"><span data-stu-id="8e52a-177">INPUTS</span></span>

## <span data-ttu-id="8e52a-178">輸出</span><span class="sxs-lookup"><span data-stu-id="8e52a-178">OUTPUTS</span></span>

### <span data-ttu-id="8e52a-179">ISite 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="8e52a-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="8e52a-180">筆記</span><span class="sxs-lookup"><span data-stu-id="8e52a-180">NOTES</span></span>

<span data-ttu-id="8e52a-181">別名</span><span class="sxs-lookup"><span data-stu-id="8e52a-181">ALIASES</span></span>

## <span data-ttu-id="8e52a-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e52a-182">RELATED LINKS</span></span>

