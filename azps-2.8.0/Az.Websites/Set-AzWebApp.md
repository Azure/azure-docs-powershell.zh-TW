---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793058"
---
# <span data-ttu-id="2f146-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-101">Set-AzWebApp</span></span>

## <span data-ttu-id="2f146-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f146-102">SYNOPSIS</span></span>
<span data-ttu-id="2f146-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="2f146-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="2f146-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f146-104">SYNTAX</span></span>

### <span data-ttu-id="2f146-105">S1</span><span class="sxs-lookup"><span data-stu-id="2f146-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f146-106">S2</span><span class="sxs-lookup"><span data-stu-id="2f146-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f146-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f146-107">DESCRIPTION</span></span>
<span data-ttu-id="2f146-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="2f146-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="2f146-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f146-109">EXAMPLES</span></span>

### <span data-ttu-id="2f146-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2f146-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="2f146-111">這個命令會變更與與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 相關聯的 appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="2f146-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="2f146-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="2f146-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="2f146-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="2f146-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="2f146-114">範例2</span><span class="sxs-lookup"><span data-stu-id="2f146-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="2f146-115">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="2f146-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2f146-116">參數</span><span class="sxs-lookup"><span data-stu-id="2f146-116">PARAMETERS</span></span>

### <span data-ttu-id="2f146-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f146-117">-AppServicePlan</span></span>
<span data-ttu-id="2f146-118">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2f146-119">-AppSettings</span></span>
<span data-ttu-id="2f146-120">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2f146-120">App Settings HashTable.</span></span> <span data-ttu-id="2f146-121">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="2f146-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f146-122">-AsJob</span></span>
<span data-ttu-id="2f146-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f146-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f146-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2f146-124">-AssignIdentity</span></span>
<span data-ttu-id="2f146-125">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="2f146-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2f146-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="2f146-127">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-127">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="2f146-128">-AzureStoragePath</span></span>
<span data-ttu-id="2f146-129">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="2f146-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="2f146-130">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="2f146-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2f146-131">-ConnectionStrings</span></span>
<span data-ttu-id="2f146-132">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="2f146-132">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="2f146-133">-ContainerImageName</span></span>
<span data-ttu-id="2f146-134">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-134">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="2f146-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="2f146-136">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="2f146-136">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="2f146-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="2f146-138">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="2f146-138">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="2f146-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="2f146-140">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-140">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2f146-141">-DefaultDocuments</span></span>
<span data-ttu-id="2f146-142">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="2f146-142">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f146-143">-DefaultProfile</span></span>
<span data-ttu-id="2f146-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f146-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f146-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2f146-146">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="2f146-146">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="2f146-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="2f146-148">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="2f146-148">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2f146-149">-HandlerMappings</span></span>
<span data-ttu-id="2f146-150">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="2f146-150">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-151">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-151">-HostNames</span></span>
<span data-ttu-id="2f146-152">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="2f146-152">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f146-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2f146-154">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="2f146-154">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2f146-155">-HttpsOnly</span></span>
<span data-ttu-id="2f146-156">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="2f146-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2f146-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="2f146-158">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-158">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-159">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-159">-Name</span></span>
<span data-ttu-id="2f146-160">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-160">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2f146-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="2f146-162">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="2f146-162">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2f146-163">-NumberOfWorkers</span></span>
<span data-ttu-id="2f146-164">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="2f146-164">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2f146-165">-PhpVersion</span></span>
<span data-ttu-id="2f146-166">Php 版本</span><span class="sxs-lookup"><span data-stu-id="2f146-166">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f146-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="2f146-168">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="2f146-168">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f146-169">-ResourceGroupName</span></span>
<span data-ttu-id="2f146-170">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2f146-170">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2f146-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2f146-172">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="2f146-172">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-173">-WebApp</span></span>
<span data-ttu-id="2f146-174">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2f146-174">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2f146-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="2f146-176">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="2f146-176">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f146-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f146-177">CommonParameters</span></span>
<span data-ttu-id="2f146-178">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f146-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f146-179">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f146-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f146-180">輸入</span><span class="sxs-lookup"><span data-stu-id="2f146-180">INPUTS</span></span>

### <span data-ttu-id="2f146-181">System.object</span><span class="sxs-lookup"><span data-stu-id="2f146-181">System.Int32</span></span>

### <span data-ttu-id="2f146-182">System.object</span><span class="sxs-lookup"><span data-stu-id="2f146-182">System.String</span></span>

### <span data-ttu-id="2f146-183">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="2f146-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f146-184">輸出</span><span class="sxs-lookup"><span data-stu-id="2f146-184">OUTPUTS</span></span>

### <span data-ttu-id="2f146-185">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="2f146-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f146-186">筆記</span><span class="sxs-lookup"><span data-stu-id="2f146-186">NOTES</span></span>

## <span data-ttu-id="2f146-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f146-187">RELATED LINKS</span></span>

[<span data-ttu-id="2f146-188">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="2f146-189">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="2f146-190">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="2f146-191">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="2f146-192">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="2f146-193">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2f146-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
