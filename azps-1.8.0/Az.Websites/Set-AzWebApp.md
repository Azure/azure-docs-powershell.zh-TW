---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614240"
---
# <span data-ttu-id="7ff72-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-101">Set-AzWebApp</span></span>



## <span data-ttu-id="7ff72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ff72-102">SYNOPSIS</span></span>

<span data-ttu-id="7ff72-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="7ff72-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="7ff72-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ff72-104">SYNTAX</span></span>



### <span data-ttu-id="7ff72-105">S1</span><span class="sxs-lookup"><span data-stu-id="7ff72-105">S1</span></span>

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



### <span data-ttu-id="7ff72-106">S2</span><span class="sxs-lookup"><span data-stu-id="7ff72-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="7ff72-107">說明</span><span class="sxs-lookup"><span data-stu-id="7ff72-107">DESCRIPTION</span></span>

<span data-ttu-id="7ff72-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="7ff72-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="7ff72-109">示例</span><span class="sxs-lookup"><span data-stu-id="7ff72-109">EXAMPLES</span></span>



### <span data-ttu-id="7ff72-110">範例1</span><span class="sxs-lookup"><span data-stu-id="7ff72-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="7ff72-111">這個命令會變更與與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 相關聯的 appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="7ff72-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="7ff72-112">使用連結 learm 變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="7ff72-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="7ff72-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7ff72-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="7ff72-114">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="7ff72-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="7ff72-115">參數</span><span class="sxs-lookup"><span data-stu-id="7ff72-115">PARAMETERS</span></span>



### <span data-ttu-id="7ff72-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7ff72-116">-AppServicePlan</span></span>

<span data-ttu-id="7ff72-117">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="7ff72-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="7ff72-118">-AppSettings</span></span>

<span data-ttu-id="7ff72-119">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="7ff72-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="7ff72-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ff72-120">-AsJob</span></span>

<span data-ttu-id="7ff72-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ff72-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="7ff72-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7ff72-122">-AssignIdentity</span></span>

<span data-ttu-id="7ff72-123">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="7ff72-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="7ff72-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="7ff72-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="7ff72-125">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="7ff72-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="7ff72-126">-AzureStoragePath</span></span>

<span data-ttu-id="7ff72-127">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="7ff72-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="7ff72-128">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="7ff72-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="7ff72-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="7ff72-129">-ConnectionStrings</span></span>

<span data-ttu-id="7ff72-130">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="7ff72-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="7ff72-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="7ff72-131">-ContainerImageName</span></span>

<span data-ttu-id="7ff72-132">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-132">Container Image Name</span></span>



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



### <span data-ttu-id="7ff72-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="7ff72-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="7ff72-134">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="7ff72-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="7ff72-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="7ff72-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="7ff72-136">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="7ff72-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="7ff72-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="7ff72-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="7ff72-138">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="7ff72-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="7ff72-139">-DefaultDocuments</span></span>

<span data-ttu-id="7ff72-140">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="7ff72-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="7ff72-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff72-141">-DefaultProfile</span></span>

<span data-ttu-id="7ff72-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ff72-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="7ff72-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ff72-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="7ff72-144">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="7ff72-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="7ff72-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="7ff72-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="7ff72-146">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="7ff72-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="7ff72-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="7ff72-147">-HandlerMappings</span></span>

<span data-ttu-id="7ff72-148">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="7ff72-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="7ff72-149">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-149">-HostNames</span></span>

<span data-ttu-id="7ff72-150">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="7ff72-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="7ff72-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ff72-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="7ff72-152">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="7ff72-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="7ff72-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7ff72-153">-HttpsOnly</span></span>

<span data-ttu-id="7ff72-154">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="7ff72-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="7ff72-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="7ff72-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="7ff72-156">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="7ff72-157">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-157">-Name</span></span>

<span data-ttu-id="7ff72-158">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-158">WebApp Name</span></span>



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



### <span data-ttu-id="7ff72-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="7ff72-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="7ff72-160">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="7ff72-160">Net Framework Version</span></span>



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



### <span data-ttu-id="7ff72-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="7ff72-161">-NumberOfWorkers</span></span>

<span data-ttu-id="7ff72-162">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="7ff72-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="7ff72-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="7ff72-163">-PhpVersion</span></span>

<span data-ttu-id="7ff72-164">Php 版本</span><span class="sxs-lookup"><span data-stu-id="7ff72-164">Php Version</span></span>



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



### <span data-ttu-id="7ff72-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="7ff72-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="7ff72-166">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="7ff72-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="7ff72-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff72-167">-ResourceGroupName</span></span>

<span data-ttu-id="7ff72-168">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="7ff72-168">Resource Group Name</span></span>



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



### <span data-ttu-id="7ff72-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="7ff72-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="7ff72-170">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="7ff72-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="7ff72-171">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-171">-WebApp</span></span>

<span data-ttu-id="7ff72-172">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="7ff72-172">WebApp Object</span></span>



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



### <span data-ttu-id="7ff72-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="7ff72-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="7ff72-174">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="7ff72-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="7ff72-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff72-175">CommonParameters</span></span>

<span data-ttu-id="7ff72-176">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ff72-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff72-177">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ff72-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="7ff72-178">輸入</span><span class="sxs-lookup"><span data-stu-id="7ff72-178">INPUTS</span></span>



### <span data-ttu-id="7ff72-179">System.object</span><span class="sxs-lookup"><span data-stu-id="7ff72-179">System.Int32</span></span>



### <span data-ttu-id="7ff72-180">System.object</span><span class="sxs-lookup"><span data-stu-id="7ff72-180">System.String</span></span>



### <span data-ttu-id="7ff72-181">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="7ff72-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="7ff72-182">輸出</span><span class="sxs-lookup"><span data-stu-id="7ff72-182">OUTPUTS</span></span>



### <span data-ttu-id="7ff72-183">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="7ff72-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="7ff72-184">筆記</span><span class="sxs-lookup"><span data-stu-id="7ff72-184">NOTES</span></span>



## <span data-ttu-id="7ff72-185">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ff72-185">RELATED LINKS</span></span>



[<span data-ttu-id="7ff72-186">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="7ff72-187">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="7ff72-188">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="7ff72-189">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="7ff72-190">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="7ff72-191">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7ff72-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

