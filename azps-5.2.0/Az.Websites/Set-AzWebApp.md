---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277899"
---
# <span data-ttu-id="80c79-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-101">Set-AzWebApp</span></span>

## <span data-ttu-id="80c79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80c79-102">SYNOPSIS</span></span>
<span data-ttu-id="80c79-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="80c79-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="80c79-104">句法</span><span class="sxs-lookup"><span data-stu-id="80c79-104">SYNTAX</span></span>

### <span data-ttu-id="80c79-105">S1</span><span class="sxs-lookup"><span data-stu-id="80c79-105">S1</span></span>
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

### <span data-ttu-id="80c79-106">S2</span><span class="sxs-lookup"><span data-stu-id="80c79-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80c79-107">說明</span><span class="sxs-lookup"><span data-stu-id="80c79-107">DESCRIPTION</span></span>
<span data-ttu-id="80c79-108">**AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="80c79-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="80c79-109">示例</span><span class="sxs-lookup"><span data-stu-id="80c79-109">EXAMPLES</span></span>

### <span data-ttu-id="80c79-110">範例1</span><span class="sxs-lookup"><span data-stu-id="80c79-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="80c79-111">這個命令會變更與與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 相關聯的 appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="80c79-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="80c79-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="80c79-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="80c79-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="80c79-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="80c79-114">範例2</span><span class="sxs-lookup"><span data-stu-id="80c79-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="80c79-115">這個命令會將與資源群組預設的 Web App ContosoWebApp 的 HttpLoggingEnabled 設定為 true （Web-WestUS）</span><span class="sxs-lookup"><span data-stu-id="80c79-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="80c79-116">範例3</span><span class="sxs-lookup"><span data-stu-id="80c79-116">Example 3</span></span>

<span data-ttu-id="80c79-117">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="80c79-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="80c79-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="80c79-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="80c79-119">範例4</span><span class="sxs-lookup"><span data-stu-id="80c79-119">Example 4</span></span>

<span data-ttu-id="80c79-120">下列範例會建立名為 myConnectionString for Web App ContosoWebApp 的連線字串。</span><span class="sxs-lookup"><span data-stu-id="80c79-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="80c79-121">這會取代 Web 應用程式 ContosoWebApp 的所有現有的連線字串。</span><span class="sxs-lookup"><span data-stu-id="80c79-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="80c79-122">參數</span><span class="sxs-lookup"><span data-stu-id="80c79-122">PARAMETERS</span></span>

### <span data-ttu-id="80c79-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="80c79-123">-AlwaysOn</span></span>
<span data-ttu-id="80c79-124">確保所有時間都會載入 web 應用程式，而不是在空閒後卸載。</span><span class="sxs-lookup"><span data-stu-id="80c79-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="80c79-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="80c79-125">-AppServicePlan</span></span>
<span data-ttu-id="80c79-126">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="80c79-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="80c79-127">-AppSettings</span></span>
<span data-ttu-id="80c79-128">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="80c79-128">App Settings HashTable.</span></span> <span data-ttu-id="80c79-129">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="80c79-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="80c79-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80c79-130">-AsJob</span></span>
<span data-ttu-id="80c79-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="80c79-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80c79-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="80c79-132">-AssignIdentity</span></span>
<span data-ttu-id="80c79-133">啟用/停用現有 azure webapp 或 functionapp 上的 MSI</span><span class="sxs-lookup"><span data-stu-id="80c79-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="80c79-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="80c79-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="80c79-135">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="80c79-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="80c79-136">-AzureStoragePath</span></span>
<span data-ttu-id="80c79-137">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="80c79-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="80c79-138">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="80c79-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="80c79-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="80c79-139">-ConnectionStrings</span></span>
<span data-ttu-id="80c79-140">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="80c79-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="80c79-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="80c79-141">-ContainerImageName</span></span>
<span data-ttu-id="80c79-142">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-142">Container Image Name</span></span>

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

### <span data-ttu-id="80c79-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="80c79-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="80c79-144">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="80c79-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="80c79-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="80c79-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="80c79-146">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="80c79-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="80c79-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="80c79-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="80c79-148">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="80c79-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="80c79-149">-DefaultDocuments</span></span>
<span data-ttu-id="80c79-150">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="80c79-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="80c79-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c79-151">-DefaultProfile</span></span>
<span data-ttu-id="80c79-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80c79-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c79-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="80c79-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="80c79-154">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="80c79-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="80c79-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="80c79-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="80c79-156">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="80c79-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="80c79-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="80c79-157">-FtpsState</span></span>
<span data-ttu-id="80c79-158">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="80c79-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="80c79-159">允許的值 [AllAllowed |已停用 |FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="80c79-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="80c79-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="80c79-160">-HandlerMappings</span></span>
<span data-ttu-id="80c79-161">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="80c79-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="80c79-162">-主機名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-162">-HostNames</span></span>
<span data-ttu-id="80c79-163">WebApp 主機名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="80c79-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="80c79-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="80c79-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="80c79-165">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="80c79-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="80c79-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="80c79-166">-HttpsOnly</span></span>
<span data-ttu-id="80c79-167">啟用/停用現有 azure webapp 或 functionapp 上的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="80c79-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="80c79-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="80c79-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="80c79-169">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="80c79-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="80c79-170">-MinTlsVersion</span></span>
<span data-ttu-id="80c79-171">SSL 要求所需的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="80c79-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="80c79-172">允許值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="80c79-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="80c79-173">-名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-173">-Name</span></span>
<span data-ttu-id="80c79-174">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-174">WebApp Name</span></span>

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

### <span data-ttu-id="80c79-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="80c79-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="80c79-176">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="80c79-176">Net Framework Version</span></span>

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

### <span data-ttu-id="80c79-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="80c79-177">-NumberOfWorkers</span></span>
<span data-ttu-id="80c79-178">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="80c79-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="80c79-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="80c79-179">-PhpVersion</span></span>
<span data-ttu-id="80c79-180">Php 版本</span><span class="sxs-lookup"><span data-stu-id="80c79-180">Php Version</span></span>

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

### <span data-ttu-id="80c79-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="80c79-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="80c79-182">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="80c79-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="80c79-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80c79-183">-ResourceGroupName</span></span>
<span data-ttu-id="80c79-184">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="80c79-184">Resource Group Name</span></span>

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

### <span data-ttu-id="80c79-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="80c79-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="80c79-186">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="80c79-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="80c79-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-187">-WebApp</span></span>
<span data-ttu-id="80c79-188">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="80c79-188">WebApp Object</span></span>

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

### <span data-ttu-id="80c79-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="80c79-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="80c79-190">WebSocketsEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="80c79-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="80c79-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c79-191">CommonParameters</span></span>
<span data-ttu-id="80c79-192">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80c79-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c79-193">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="80c79-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c79-194">輸入</span><span class="sxs-lookup"><span data-stu-id="80c79-194">INPUTS</span></span>

### <span data-ttu-id="80c79-195">System.object</span><span class="sxs-lookup"><span data-stu-id="80c79-195">System.Int32</span></span>

### <span data-ttu-id="80c79-196">System.object</span><span class="sxs-lookup"><span data-stu-id="80c79-196">System.String</span></span>

### <span data-ttu-id="80c79-197">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="80c79-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="80c79-198">輸出</span><span class="sxs-lookup"><span data-stu-id="80c79-198">OUTPUTS</span></span>

### <span data-ttu-id="80c79-199">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="80c79-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="80c79-200">筆記</span><span class="sxs-lookup"><span data-stu-id="80c79-200">NOTES</span></span>
<span data-ttu-id="80c79-201">下面提供的 Cmdlet 可協助您將 Azure Web App 更新為 **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="80c79-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="80c79-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-WestUS"-ResourceType Microsoft. Web/網站/config-"ContosoWebApp/metadata"-ApiVersion 2018-02-01-強制</span><span class="sxs-lookup"><span data-stu-id="80c79-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="80c79-203">將預設網頁 WestUS 的值以 webapp 和 ContosoWebApp 的資源群組名稱取代為 webapp 名稱。</span><span class="sxs-lookup"><span data-stu-id="80c79-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="80c79-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="80c79-204">RELATED LINKS</span></span>

[<span data-ttu-id="80c79-205">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="80c79-206">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="80c79-207">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="80c79-208">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="80c79-209">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="80c79-210">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="80c79-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="80c79-211">新-AzResource</span><span class="sxs-lookup"><span data-stu-id="80c79-211">New-AzResource</span></span>](./New-AzResource.md)
