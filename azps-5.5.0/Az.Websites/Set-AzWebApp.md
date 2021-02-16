---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 5594e43b2e6c67e9df5b526f753557edd8a4d5ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414725"
---
# <span data-ttu-id="c7dfd-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-101">Set-AzWebApp</span></span>

## <span data-ttu-id="c7dfd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c7dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="c7dfd-103">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="c7dfd-104">語法</span><span class="sxs-lookup"><span data-stu-id="c7dfd-104">SYNTAX</span></span>

### <span data-ttu-id="c7dfd-105">S1</span><span class="sxs-lookup"><span data-stu-id="c7dfd-105">S1</span></span>
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

### <span data-ttu-id="c7dfd-106">S2</span><span class="sxs-lookup"><span data-stu-id="c7dfd-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7dfd-107">描述</span><span class="sxs-lookup"><span data-stu-id="c7dfd-107">DESCRIPTION</span></span>
<span data-ttu-id="c7dfd-108">**Set-AzWebApp** Cmdlet 會設定 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c7dfd-109">例子</span><span class="sxs-lookup"><span data-stu-id="c7dfd-109">EXAMPLES</span></span>

### <span data-ttu-id="c7dfd-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c7dfd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c7dfd-111">此命令會變更與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp 相關應用程式服務計畫。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c7dfd-112">使用連結深入瞭解如何變更應用程式服務計畫和與其相關聯的限制式。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c7dfd-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c7dfd-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c7dfd-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="c7dfd-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c7dfd-115">此命令將與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp 的 HTTPLoggingEnabled 設定為 True</span><span class="sxs-lookup"><span data-stu-id="c7dfd-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c7dfd-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="c7dfd-116">Example 3</span></span>

<span data-ttu-id="c7dfd-117">修改 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="c7dfd-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="c7dfd-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="c7dfd-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="c7dfd-119">Example 4</span></span>

<span data-ttu-id="c7dfd-120">下列範例會建立一個名為 myConnectionString for Web App ContosoWebApp 的連接字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="c7dfd-121">這會取代 Web App ContosoWebApp 的所有現有連接字串。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="c7dfd-122">參數</span><span class="sxs-lookup"><span data-stu-id="c7dfd-122">PARAMETERS</span></span>

### <span data-ttu-id="c7dfd-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c7dfd-123">-AlwaysOn</span></span>
<span data-ttu-id="c7dfd-124">確保 Web App 會一直載入，而不是閒置後卸貨。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c7dfd-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7dfd-125">-AppServicePlan</span></span>
<span data-ttu-id="c7dfd-126">應用程式服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="c7dfd-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c7dfd-127">-AppSettings</span></span>
<span data-ttu-id="c7dfd-128">應用程式設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-128">App Settings HashTable.</span></span> <span data-ttu-id="c7dfd-129">現有的應用程式設定將會取代，移除未提供的任何設定。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="c7dfd-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7dfd-130">-AsJob</span></span>
<span data-ttu-id="c7dfd-131">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c7dfd-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7dfd-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c7dfd-132">-AssignIdentity</span></span>
<span data-ttu-id="c7dfd-133">在現有的 Azure Webapp 或函數應用程式上啟用/停用 MSI</span><span class="sxs-lookup"><span data-stu-id="c7dfd-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c7dfd-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c7dfd-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="c7dfd-135">自動交換的目的地插槽名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c7dfd-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c7dfd-136">-AzureStoragePath</span></span>
<span data-ttu-id="c7dfd-137">要安裝在容器用 Web App 內的 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c7dfd-138">使用New-AzureRmWebAppAzureStoragePath建立</span><span class="sxs-lookup"><span data-stu-id="c7dfd-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c7dfd-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c7dfd-139">-ConnectionStrings</span></span>
<span data-ttu-id="c7dfd-140">連接字串雜湊表</span><span class="sxs-lookup"><span data-stu-id="c7dfd-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c7dfd-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c7dfd-141">-ContainerImageName</span></span>
<span data-ttu-id="c7dfd-142">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-142">Container Image Name</span></span>

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

### <span data-ttu-id="c7dfd-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c7dfd-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c7dfd-144">私人容器登錄密碼</span><span class="sxs-lookup"><span data-stu-id="c7dfd-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c7dfd-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c7dfd-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c7dfd-146">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="c7dfd-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c7dfd-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c7dfd-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="c7dfd-148">私人容器登錄使用者名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c7dfd-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c7dfd-149">-DefaultDocuments</span></span>
<span data-ttu-id="c7dfd-150">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="c7dfd-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="c7dfd-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7dfd-151">-DefaultProfile</span></span>
<span data-ttu-id="c7dfd-152">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7dfd-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7dfd-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c7dfd-154">啟用布林值的詳細錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="c7dfd-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c7dfd-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c7dfd-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c7dfd-156">啟用/停用容器連續部署網頁元件</span><span class="sxs-lookup"><span data-stu-id="c7dfd-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c7dfd-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c7dfd-157">-FtpsState</span></span>
<span data-ttu-id="c7dfd-158">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c7dfd-159">允許的值 [全部|已停用|FtpsOnly]。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c7dfd-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c7dfd-160">-HandlerMappings</span></span>
<span data-ttu-id="c7dfd-161">處理常式地圖 IList</span><span class="sxs-lookup"><span data-stu-id="c7dfd-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c7dfd-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="c7dfd-162">-HostNames</span></span>
<span data-ttu-id="c7dfd-163">WebApp HostNames 字串陣列</span><span class="sxs-lookup"><span data-stu-id="c7dfd-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="c7dfd-164">-HTTPLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7dfd-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c7dfd-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c7dfd-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c7dfd-166">-HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="c7dfd-166">-HttpsOnly</span></span>
<span data-ttu-id="c7dfd-167">啟用/停用將現有 Azure Webapp 或函數應用程式上的所有流量重新導向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="c7dfd-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c7dfd-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c7dfd-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="c7dfd-169">受管理的管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c7dfd-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c7dfd-170">-MinTlsVersion</span></span>
<span data-ttu-id="c7dfd-171">SSL 要求所需的 TLS 最低版本。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c7dfd-172">允許的值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c7dfd-173">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-173">-Name</span></span>
<span data-ttu-id="c7dfd-174">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c7dfd-174">WebApp Name</span></span>

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

### <span data-ttu-id="c7dfd-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c7dfd-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="c7dfd-176">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="c7dfd-176">Net Framework Version</span></span>

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

### <span data-ttu-id="c7dfd-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c7dfd-177">-NumberOfWorkers</span></span>
<span data-ttu-id="c7dfd-178">要配置的員工人數</span><span class="sxs-lookup"><span data-stu-id="c7dfd-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c7dfd-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c7dfd-179">-PhpVersion</span></span>
<span data-ttu-id="c7dfd-180">Php 版本</span><span class="sxs-lookup"><span data-stu-id="c7dfd-180">Php Version</span></span>

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

### <span data-ttu-id="c7dfd-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7dfd-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="c7dfd-182">已啟用要求追蹤</span><span class="sxs-lookup"><span data-stu-id="c7dfd-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="c7dfd-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7dfd-183">-ResourceGroupName</span></span>
<span data-ttu-id="c7dfd-184">資源組名</span><span class="sxs-lookup"><span data-stu-id="c7dfd-184">Resource Group Name</span></span>

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

### <span data-ttu-id="c7dfd-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c7dfd-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c7dfd-186">使用 32 位的工作程式布林值</span><span class="sxs-lookup"><span data-stu-id="c7dfd-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c7dfd-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-187">-WebApp</span></span>
<span data-ttu-id="c7dfd-188">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c7dfd-188">WebApp Object</span></span>

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

### <span data-ttu-id="c7dfd-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c7dfd-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="c7dfd-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c7dfd-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="c7dfd-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7dfd-191">CommonParameters</span></span>
<span data-ttu-id="c7dfd-192">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7dfd-193">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7dfd-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7dfd-194">輸入</span><span class="sxs-lookup"><span data-stu-id="c7dfd-194">INPUTS</span></span>

### <span data-ttu-id="c7dfd-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c7dfd-195">System.Int32</span></span>

### <span data-ttu-id="c7dfd-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c7dfd-196">System.String</span></span>

### <span data-ttu-id="c7dfd-197">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c7dfd-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7dfd-198">輸出</span><span class="sxs-lookup"><span data-stu-id="c7dfd-198">OUTPUTS</span></span>

### <span data-ttu-id="c7dfd-199">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c7dfd-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7dfd-200">筆記</span><span class="sxs-lookup"><span data-stu-id="c7dfd-200">NOTES</span></span>
<span data-ttu-id="c7dfd-201">以下提供的 Cmdlet 可協助您將 Azure Web App 更新為 **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="c7dfd-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="c7dfd-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="c7dfd-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="c7dfd-203">以 Webapp 和 ContosoWebApp 的資源組名取代 Default-Web-WestUS 的值。</span><span class="sxs-lookup"><span data-stu-id="c7dfd-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="c7dfd-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7dfd-204">RELATED LINKS</span></span>

[<span data-ttu-id="c7dfd-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c7dfd-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c7dfd-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c7dfd-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c7dfd-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c7dfd-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7dfd-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

