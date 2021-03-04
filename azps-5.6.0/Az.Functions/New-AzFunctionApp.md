---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 97a1fa7aa5488034fa1f0147ae5a06ff639ecc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906186"
---
# <span data-ttu-id="a053f-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a053f-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="a053f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a053f-102">SYNOPSIS</span></span>
<span data-ttu-id="a053f-103">建立函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-103">Creates a function app.</span></span>

## <span data-ttu-id="a053f-104">語法</span><span class="sxs-lookup"><span data-stu-id="a053f-104">SYNTAX</span></span>

### <span data-ttu-id="a053f-105">消費 (預設) </span><span class="sxs-lookup"><span data-stu-id="a053f-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a053f-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a053f-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a053f-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="a053f-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a053f-108">描述</span><span class="sxs-lookup"><span data-stu-id="a053f-108">DESCRIPTION</span></span>
<span data-ttu-id="a053f-109">建立函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-109">Creates a function app.</span></span>

## <span data-ttu-id="a053f-110">例子</span><span class="sxs-lookup"><span data-stu-id="a053f-110">EXAMPLES</span></span>

### <span data-ttu-id="a053f-111">範例 1：在中美國建立消費 PowerShell 函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="a053f-112">此命令會在美國中央建立一個消費 PowerShell 函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="a053f-113">範例 2：建立將在服務方案中託管的 PowerShell 函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="a053f-114">此命令會建立一個 PowerShell 函數應用程式，它將託管在服務方案中。</span><span class="sxs-lookup"><span data-stu-id="a053f-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="a053f-115">範例 3：使用私人 ACR 影像建立函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="a053f-116">此命令會使用私人 ACR 圖像建立函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="a053f-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="a053f-117">參數</span><span class="sxs-lookup"><span data-stu-id="a053f-117">PARAMETERS</span></span>

### <span data-ttu-id="a053f-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="a053f-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="a053f-119">要新增之應用程式深入資訊的應用程式便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a053f-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="a053f-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="a053f-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="a053f-121">要新加入函數 App 的現有 App 深入資訊專案名稱。</span><span class="sxs-lookup"><span data-stu-id="a053f-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="a053f-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="a053f-122">-AppSetting</span></span>
<span data-ttu-id="a053f-123">函數應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="a053f-123">Function app settings.</span></span>

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

### <span data-ttu-id="a053f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a053f-124">-AsJob</span></span>
<span data-ttu-id="a053f-125">執行 Cmdlet 做為背景工作。</span><span class="sxs-lookup"><span data-stu-id="a053f-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="a053f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a053f-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="a053f-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a053f-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="a053f-128">在建立功能應用程式期間停用建立應用程式深入資訊資源。</span><span class="sxs-lookup"><span data-stu-id="a053f-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="a053f-129">沒有可用的記錄。</span><span class="sxs-lookup"><span data-stu-id="a053f-129">No logs will be available.</span></span>

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

### <span data-ttu-id="a053f-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="a053f-130">-DockerImageName</span></span>
<span data-ttu-id="a053f-131">僅適用于 Linux。</span><span class="sxs-lookup"><span data-stu-id="a053f-131">Linux only.</span></span>
<span data-ttu-id="a053f-132">來自 Docker Registry 的容器圖像名稱，例如 publisher/image-name：tag。</span><span class="sxs-lookup"><span data-stu-id="a053f-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="a053f-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="a053f-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="a053f-134">容器登錄使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="a053f-134">The container registry user name and password.</span></span>
<span data-ttu-id="a053f-135">這是私人註冊的必填專案。</span><span class="sxs-lookup"><span data-stu-id="a053f-135">Required for private registries.</span></span>

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

### <span data-ttu-id="a053f-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="a053f-136">-FunctionsVersion</span></span>
<span data-ttu-id="a053f-137">函數版本。</span><span class="sxs-lookup"><span data-stu-id="a053f-137">The Functions version.</span></span>

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

### <span data-ttu-id="a053f-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="a053f-138">-IdentityID</span></span>
<span data-ttu-id="a053f-139">指定與函數應用程式相關聯的使用者身分清單。</span><span class="sxs-lookup"><span data-stu-id="a053f-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="a053f-140">使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="a053f-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="a053f-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a053f-141">-IdentityType</span></span>
<span data-ttu-id="a053f-142">指定函數應用程式所使用的身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="a053f-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="a053f-143">此參數可接受的值為：- SystemAssigned - UserAssigned</span><span class="sxs-lookup"><span data-stu-id="a053f-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="a053f-144">-位置</span><span class="sxs-lookup"><span data-stu-id="a053f-144">-Location</span></span>
<span data-ttu-id="a053f-145">消費方案的位置。</span><span class="sxs-lookup"><span data-stu-id="a053f-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="a053f-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="a053f-146">-Name</span></span>
<span data-ttu-id="a053f-147">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a053f-147">The name of the function app.</span></span>

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

### <span data-ttu-id="a053f-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a053f-148">-NoWait</span></span>
<span data-ttu-id="a053f-149">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="a053f-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="a053f-150">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="a053f-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a053f-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="a053f-151">-OSType</span></span>
<span data-ttu-id="a053f-152">主託管函數應用程式的 OS。</span><span class="sxs-lookup"><span data-stu-id="a053f-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="a053f-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a053f-153">-PassThru</span></span>
<span data-ttu-id="a053f-154">命令成功時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a053f-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="a053f-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="a053f-155">-PlanName</span></span>
<span data-ttu-id="a053f-156">服務方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="a053f-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="a053f-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a053f-157">-ResourceGroupName</span></span>
<span data-ttu-id="a053f-158">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a053f-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="a053f-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="a053f-159">-Runtime</span></span>
<span data-ttu-id="a053f-160">函數執行時間。</span><span class="sxs-lookup"><span data-stu-id="a053f-160">The function runtime.</span></span>

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

### <span data-ttu-id="a053f-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="a053f-161">-RuntimeVersion</span></span>
<span data-ttu-id="a053f-162">函數執行時間。</span><span class="sxs-lookup"><span data-stu-id="a053f-162">The function runtime.</span></span>

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

### <span data-ttu-id="a053f-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a053f-163">-StorageAccountName</span></span>
<span data-ttu-id="a053f-164">儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a053f-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="a053f-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a053f-165">-SubscriptionId</span></span>
<span data-ttu-id="a053f-166">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="a053f-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a053f-167">-標記</span><span class="sxs-lookup"><span data-stu-id="a053f-167">-Tag</span></span>
<span data-ttu-id="a053f-168">資源標記。</span><span class="sxs-lookup"><span data-stu-id="a053f-168">Resource tags.</span></span>

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

### <span data-ttu-id="a053f-169">-確認</span><span class="sxs-lookup"><span data-stu-id="a053f-169">-Confirm</span></span>
<span data-ttu-id="a053f-170">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a053f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a053f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a053f-171">-WhatIf</span></span>
<span data-ttu-id="a053f-172">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a053f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a053f-173">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a053f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a053f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a053f-174">CommonParameters</span></span>
<span data-ttu-id="a053f-175">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a053f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a053f-176">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a053f-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a053f-177">輸入</span><span class="sxs-lookup"><span data-stu-id="a053f-177">INPUTS</span></span>

## <span data-ttu-id="a053f-178">輸出</span><span class="sxs-lookup"><span data-stu-id="a053f-178">OUTPUTS</span></span>

### <span data-ttu-id="a053f-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="a053f-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="a053f-180">筆記</span><span class="sxs-lookup"><span data-stu-id="a053f-180">NOTES</span></span>

<span data-ttu-id="a053f-181">別名</span><span class="sxs-lookup"><span data-stu-id="a053f-181">ALIASES</span></span>

## <span data-ttu-id="a053f-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="a053f-182">RELATED LINKS</span></span>

