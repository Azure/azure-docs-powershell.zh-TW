---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970741"
---
# <span data-ttu-id="17675-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-101">Set-AzWebApp</span></span>

## <span data-ttu-id="17675-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17675-102">SYNOPSIS</span></span>
<span data-ttu-id="17675-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="17675-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="17675-104">句法</span><span class="sxs-lookup"><span data-stu-id="17675-104">SYNTAX</span></span>

### <span data-ttu-id="17675-105">S1</span><span class="sxs-lookup"><span data-stu-id="17675-105">S1</span></span>
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
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17675-106">S2</span><span class="sxs-lookup"><span data-stu-id="17675-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17675-107">說明</span><span class="sxs-lookup"><span data-stu-id="17675-107">DESCRIPTION</span></span>
<span data-ttu-id="17675-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="17675-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="17675-109">示例</span><span class="sxs-lookup"><span data-stu-id="17675-109">EXAMPLES</span></span>

### <span data-ttu-id="17675-110">範例1</span><span class="sxs-lookup"><span data-stu-id="17675-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="17675-111">這個命令會變更與與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 相關聯的 appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="17675-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="17675-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="17675-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="17675-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="17675-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="17675-114">範例2</span><span class="sxs-lookup"><span data-stu-id="17675-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="17675-115">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="17675-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="17675-116">範例3</span><span class="sxs-lookup"><span data-stu-id="17675-116">Example 3</span></span>

<span data-ttu-id="17675-117">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="17675-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="17675-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="17675-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="17675-119">參數</span><span class="sxs-lookup"><span data-stu-id="17675-119">PARAMETERS</span></span>

### <span data-ttu-id="17675-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="17675-120">-AlwaysOn</span></span>
<span data-ttu-id="17675-121">確保所有時間都會載入 web 應用程式，而不是在空閒後卸載。</span><span class="sxs-lookup"><span data-stu-id="17675-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="17675-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="17675-122">-AppServicePlan</span></span>
<span data-ttu-id="17675-123">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="17675-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="17675-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="17675-124">-AppSettings</span></span>
<span data-ttu-id="17675-125">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="17675-125">App Settings HashTable.</span></span> <span data-ttu-id="17675-126">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="17675-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="17675-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17675-127">-AsJob</span></span>
<span data-ttu-id="17675-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="17675-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17675-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="17675-129">-AssignIdentity</span></span>
<span data-ttu-id="17675-130">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="17675-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="17675-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="17675-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="17675-132">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="17675-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="17675-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="17675-133">-AzureStoragePath</span></span>
<span data-ttu-id="17675-134">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="17675-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="17675-135">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="17675-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="17675-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="17675-136">-ConnectionStrings</span></span>
<span data-ttu-id="17675-137">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="17675-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="17675-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="17675-138">-ContainerImageName</span></span>
<span data-ttu-id="17675-139">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="17675-139">Container Image Name</span></span>

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

### <span data-ttu-id="17675-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="17675-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="17675-141">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="17675-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="17675-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="17675-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="17675-143">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="17675-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="17675-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="17675-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="17675-145">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="17675-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="17675-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="17675-146">-DefaultDocuments</span></span>
<span data-ttu-id="17675-147">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="17675-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="17675-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17675-148">-DefaultProfile</span></span>
<span data-ttu-id="17675-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17675-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17675-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="17675-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="17675-151">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="17675-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="17675-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="17675-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="17675-153">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="17675-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="17675-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="17675-154">-FtpsState</span></span>
<span data-ttu-id="17675-155">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="17675-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="17675-156">允許的值 [AllAllowed |已停用 |FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="17675-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="17675-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="17675-157">-HandlerMappings</span></span>
<span data-ttu-id="17675-158">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="17675-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="17675-159">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="17675-159">-HostNames</span></span>
<span data-ttu-id="17675-160">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="17675-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="17675-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="17675-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="17675-162">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="17675-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="17675-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="17675-163">-HttpsOnly</span></span>
<span data-ttu-id="17675-164">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="17675-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="17675-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="17675-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="17675-166">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="17675-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="17675-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="17675-167">-MinTlsVersion</span></span>
<span data-ttu-id="17675-168">SSL 要求所需的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="17675-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="17675-169">允許值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="17675-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="17675-170">-名稱</span><span class="sxs-lookup"><span data-stu-id="17675-170">-Name</span></span>
<span data-ttu-id="17675-171">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="17675-171">WebApp Name</span></span>

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

### <span data-ttu-id="17675-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="17675-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="17675-173">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="17675-173">Net Framework Version</span></span>

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

### <span data-ttu-id="17675-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="17675-174">-NumberOfWorkers</span></span>
<span data-ttu-id="17675-175">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="17675-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="17675-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="17675-176">-PhpVersion</span></span>
<span data-ttu-id="17675-177">Php 版本</span><span class="sxs-lookup"><span data-stu-id="17675-177">Php Version</span></span>

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

### <span data-ttu-id="17675-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="17675-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="17675-179">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="17675-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="17675-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17675-180">-ResourceGroupName</span></span>
<span data-ttu-id="17675-181">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="17675-181">Resource Group Name</span></span>

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

### <span data-ttu-id="17675-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="17675-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="17675-183">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="17675-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="17675-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="17675-184">-WebApp</span></span>
<span data-ttu-id="17675-185">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="17675-185">WebApp Object</span></span>

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

### <span data-ttu-id="17675-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="17675-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="17675-187">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="17675-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="17675-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17675-188">CommonParameters</span></span>
<span data-ttu-id="17675-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17675-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17675-190">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17675-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17675-191">輸入</span><span class="sxs-lookup"><span data-stu-id="17675-191">INPUTS</span></span>

### <span data-ttu-id="17675-192">System.object</span><span class="sxs-lookup"><span data-stu-id="17675-192">System.Int32</span></span>

### <span data-ttu-id="17675-193">System.object</span><span class="sxs-lookup"><span data-stu-id="17675-193">System.String</span></span>

### <span data-ttu-id="17675-194">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="17675-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17675-195">輸出</span><span class="sxs-lookup"><span data-stu-id="17675-195">OUTPUTS</span></span>

### <span data-ttu-id="17675-196">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="17675-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="17675-197">筆記</span><span class="sxs-lookup"><span data-stu-id="17675-197">NOTES</span></span>
<span data-ttu-id="17675-198">下面提供的 Cmdlet 可協助您將 Azure Web App 更新為 **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="17675-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="17675-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-WestUS"-ResourceType Microsoft. Web/網站/config-"ContosoWebApp/metadata"-ApiVersion 2018-02-01-強制</span><span class="sxs-lookup"><span data-stu-id="17675-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="17675-200">將預設網頁 WestUS 的值以 webapp 和 ContosoWebApp 的資源群組名稱取代為 webapp 名稱。</span><span class="sxs-lookup"><span data-stu-id="17675-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="17675-201">相關連結</span><span class="sxs-lookup"><span data-stu-id="17675-201">RELATED LINKS</span></span>

[<span data-ttu-id="17675-202">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="17675-203">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="17675-204">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="17675-205">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="17675-206">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="17675-207">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="17675-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="17675-208">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="17675-208">New-AzResource</span></span>](./New-AzResource.md)
