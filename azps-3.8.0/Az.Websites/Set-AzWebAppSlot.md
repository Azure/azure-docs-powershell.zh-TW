---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958543"
---
# <span data-ttu-id="632ee-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="632ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="632ee-102">SYNOPSIS</span></span>
<span data-ttu-id="632ee-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="632ee-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="632ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="632ee-104">SYNTAX</span></span>

### <span data-ttu-id="632ee-105">S1</span><span class="sxs-lookup"><span data-stu-id="632ee-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="632ee-106">S2</span><span class="sxs-lookup"><span data-stu-id="632ee-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632ee-107">說明</span><span class="sxs-lookup"><span data-stu-id="632ee-107">DESCRIPTION</span></span>
<span data-ttu-id="632ee-108">**AzWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="632ee-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="632ee-109">示例</span><span class="sxs-lookup"><span data-stu-id="632ee-109">EXAMPLES</span></span>

### <span data-ttu-id="632ee-110">範例1</span><span class="sxs-lookup"><span data-stu-id="632ee-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="632ee-111">這個命令會變更與 Slot001 相關聯的 appservice 方案（與資源群組預設-Web-WestUS 相關的 Webapp ContosoWebApp）。</span><span class="sxs-lookup"><span data-stu-id="632ee-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="632ee-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="632ee-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="632ee-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="632ee-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="632ee-114">範例2</span><span class="sxs-lookup"><span data-stu-id="632ee-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="632ee-115">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="632ee-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="632ee-116">參數</span><span class="sxs-lookup"><span data-stu-id="632ee-116">PARAMETERS</span></span>

### <span data-ttu-id="632ee-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="632ee-117">-AlwaysOn</span></span>
<span data-ttu-id="632ee-118">確保所有時間都會載入 web 應用程式，而不是在空閒後卸載。</span><span class="sxs-lookup"><span data-stu-id="632ee-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="632ee-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="632ee-119">-AppServicePlan</span></span>
<span data-ttu-id="632ee-120">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-120">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="632ee-121">-AppSettings</span></span>
<span data-ttu-id="632ee-122">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="632ee-122">App Settings HashTable.</span></span> <span data-ttu-id="632ee-123">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="632ee-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="632ee-124">-AsJob</span></span>
<span data-ttu-id="632ee-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="632ee-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="632ee-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="632ee-126">-AssignIdentity</span></span>
<span data-ttu-id="632ee-127">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="632ee-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="632ee-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="632ee-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="632ee-129">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-129">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="632ee-130">-AzureStoragePath</span></span>
<span data-ttu-id="632ee-131">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="632ee-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="632ee-132">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="632ee-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="632ee-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="632ee-133">-ConnectionStrings</span></span>
<span data-ttu-id="632ee-134">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="632ee-134">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="632ee-135">-ContainerImageName</span></span>
<span data-ttu-id="632ee-136">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-136">Container Image Name</span></span>

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

### <span data-ttu-id="632ee-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="632ee-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="632ee-138">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="632ee-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="632ee-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="632ee-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="632ee-140">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="632ee-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="632ee-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="632ee-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="632ee-142">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="632ee-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="632ee-143">-DefaultDocuments</span></span>
<span data-ttu-id="632ee-144">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="632ee-144">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632ee-145">-DefaultProfile</span></span>
<span data-ttu-id="632ee-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="632ee-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="632ee-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="632ee-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="632ee-148">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="632ee-148">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="632ee-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="632ee-150">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="632ee-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="632ee-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="632ee-151">-FtpsState</span></span>
<span data-ttu-id="632ee-152">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="632ee-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="632ee-153">允許的值 [AllAllowed |已停用 |FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="632ee-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="632ee-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="632ee-154">-HandlerMappings</span></span>
<span data-ttu-id="632ee-155">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="632ee-155">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="632ee-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="632ee-157">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="632ee-157">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="632ee-158">-HttpsOnly</span></span>
<span data-ttu-id="632ee-159">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="632ee-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="632ee-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="632ee-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="632ee-161">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-161">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="632ee-162">-MinTlsVersion</span></span>
<span data-ttu-id="632ee-163">SSL 要求所需的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="632ee-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="632ee-164">允許值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="632ee-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="632ee-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-165">-Name</span></span>
<span data-ttu-id="632ee-166">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-166">WebApp Name</span></span>

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

### <span data-ttu-id="632ee-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="632ee-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="632ee-168">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="632ee-168">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="632ee-169">-NumberOfWorkers</span></span>
<span data-ttu-id="632ee-170">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="632ee-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="632ee-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="632ee-171">-PhpVersion</span></span>
<span data-ttu-id="632ee-172">Php 版本</span><span class="sxs-lookup"><span data-stu-id="632ee-172">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="632ee-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="632ee-174">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="632ee-174">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632ee-175">-ResourceGroupName</span></span>
<span data-ttu-id="632ee-176">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-176">Resource Group Name</span></span>

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

### <span data-ttu-id="632ee-177">-槽</span><span class="sxs-lookup"><span data-stu-id="632ee-177">-Slot</span></span>
<span data-ttu-id="632ee-178">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="632ee-178">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="632ee-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="632ee-180">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="632ee-180">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="632ee-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="632ee-181">-WebApp</span></span>
<span data-ttu-id="632ee-182">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="632ee-182">WebApp Object</span></span>

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

### <span data-ttu-id="632ee-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="632ee-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="632ee-184">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="632ee-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="632ee-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632ee-185">CommonParameters</span></span>
<span data-ttu-id="632ee-186">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="632ee-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632ee-187">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="632ee-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632ee-188">輸入</span><span class="sxs-lookup"><span data-stu-id="632ee-188">INPUTS</span></span>

### <span data-ttu-id="632ee-189">System.object</span><span class="sxs-lookup"><span data-stu-id="632ee-189">System.Int32</span></span>

### <span data-ttu-id="632ee-190">System.object</span><span class="sxs-lookup"><span data-stu-id="632ee-190">System.String</span></span>

### <span data-ttu-id="632ee-191">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="632ee-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="632ee-192">輸出</span><span class="sxs-lookup"><span data-stu-id="632ee-192">OUTPUTS</span></span>

### <span data-ttu-id="632ee-193">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="632ee-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="632ee-194">筆記</span><span class="sxs-lookup"><span data-stu-id="632ee-194">NOTES</span></span>

## <span data-ttu-id="632ee-195">相關連結</span><span class="sxs-lookup"><span data-stu-id="632ee-195">RELATED LINKS</span></span>

[<span data-ttu-id="632ee-196">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="632ee-197">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="632ee-198">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="632ee-199">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="632ee-200">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="632ee-201">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="632ee-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="632ee-202">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="632ee-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
