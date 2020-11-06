---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448865"
---
# <span data-ttu-id="2de4b-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="2de4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2de4b-102">SYNOPSIS</span></span>
<span data-ttu-id="2de4b-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="2de4b-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2de4b-104">SYNTAX</span></span>

### <span data-ttu-id="2de4b-105">S1</span><span class="sxs-lookup"><span data-stu-id="2de4b-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de4b-106">S2</span><span class="sxs-lookup"><span data-stu-id="2de4b-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2de4b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2de4b-107">DESCRIPTION</span></span>
<span data-ttu-id="2de4b-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="2de4b-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="2de4b-109">示例</span><span class="sxs-lookup"><span data-stu-id="2de4b-109">EXAMPLES</span></span>

### <span data-ttu-id="2de4b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2de4b-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="2de4b-111">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="2de4b-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2de4b-112">參數</span><span class="sxs-lookup"><span data-stu-id="2de4b-112">PARAMETERS</span></span>

### <span data-ttu-id="2de4b-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2de4b-113">-AppServicePlan</span></span>
<span data-ttu-id="2de4b-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="2de4b-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2de4b-115">-AppSettings</span></span>
<span data-ttu-id="2de4b-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="2de4b-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="2de4b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2de4b-117">-AsJob</span></span>
<span data-ttu-id="2de4b-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2de4b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2de4b-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2de4b-119">-AssignIdentity</span></span>
<span data-ttu-id="2de4b-120">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="2de4b-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="2de4b-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2de4b-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="2de4b-122">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="2de4b-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2de4b-123">-ConnectionStrings</span></span>
<span data-ttu-id="2de4b-124">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="2de4b-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="2de4b-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="2de4b-125">-ContainerImageName</span></span>
<span data-ttu-id="2de4b-126">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-126">Container Image Name</span></span>

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

### <span data-ttu-id="2de4b-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="2de4b-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="2de4b-128">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="2de4b-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="2de4b-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="2de4b-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="2de4b-130">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="2de4b-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="2de4b-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="2de4b-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="2de4b-132">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="2de4b-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2de4b-133">-DefaultDocuments</span></span>
<span data-ttu-id="2de4b-134">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="2de4b-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="2de4b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de4b-135">-DefaultProfile</span></span>
<span data-ttu-id="2de4b-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2de4b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de4b-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2de4b-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2de4b-138">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="2de4b-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="2de4b-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="2de4b-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="2de4b-140">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="2de4b-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="2de4b-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2de4b-141">-HandlerMappings</span></span>
<span data-ttu-id="2de4b-142">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="2de4b-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="2de4b-143">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-143">-HostNames</span></span>
<span data-ttu-id="2de4b-144">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="2de4b-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="2de4b-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2de4b-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2de4b-146">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="2de4b-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="2de4b-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2de4b-147">-HttpsOnly</span></span>
<span data-ttu-id="2de4b-148">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="2de4b-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="2de4b-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2de4b-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="2de4b-150">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="2de4b-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-151">-Name</span></span>
<span data-ttu-id="2de4b-152">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-152">WebApp Name</span></span>

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

### <span data-ttu-id="2de4b-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2de4b-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="2de4b-154">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="2de4b-154">Net Framework Version</span></span>

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

### <span data-ttu-id="2de4b-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2de4b-155">-NumberOfWorkers</span></span>
<span data-ttu-id="2de4b-156">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="2de4b-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="2de4b-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2de4b-157">-PhpVersion</span></span>
<span data-ttu-id="2de4b-158">Php 版本</span><span class="sxs-lookup"><span data-stu-id="2de4b-158">Php Version</span></span>

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

### <span data-ttu-id="2de4b-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2de4b-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="2de4b-160">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="2de4b-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="2de4b-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de4b-161">-ResourceGroupName</span></span>
<span data-ttu-id="2de4b-162">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2de4b-162">Resource Group Name</span></span>

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

### <span data-ttu-id="2de4b-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2de4b-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2de4b-164">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="2de4b-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="2de4b-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-165">-WebApp</span></span>
<span data-ttu-id="2de4b-166">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2de4b-166">WebApp Object</span></span>

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

### <span data-ttu-id="2de4b-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2de4b-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="2de4b-168">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="2de4b-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="2de4b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de4b-169">CommonParameters</span></span>
<span data-ttu-id="2de4b-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2de4b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de4b-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2de4b-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de4b-172">輸入</span><span class="sxs-lookup"><span data-stu-id="2de4b-172">INPUTS</span></span>

### <span data-ttu-id="2de4b-173">System.object</span><span class="sxs-lookup"><span data-stu-id="2de4b-173">System.Int32</span></span>
<span data-ttu-id="2de4b-174">參數： NumberOfWorkers (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2de4b-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="2de4b-175">System.object</span><span class="sxs-lookup"><span data-stu-id="2de4b-175">System.String</span></span>

### <span data-ttu-id="2de4b-176">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="2de4b-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="2de4b-177">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2de4b-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="2de4b-178">輸出</span><span class="sxs-lookup"><span data-stu-id="2de4b-178">OUTPUTS</span></span>

### <span data-ttu-id="2de4b-179">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="2de4b-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="2de4b-180">筆記</span><span class="sxs-lookup"><span data-stu-id="2de4b-180">NOTES</span></span>

## <span data-ttu-id="2de4b-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="2de4b-181">RELATED LINKS</span></span>

[<span data-ttu-id="2de4b-182">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="2de4b-183">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="2de4b-184">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="2de4b-185">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="2de4b-186">開始-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="2de4b-187">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="2de4b-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
