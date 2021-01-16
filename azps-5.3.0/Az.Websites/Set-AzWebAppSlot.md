---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435953"
---
# <span data-ttu-id="437cc-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="437cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="437cc-102">SYNOPSIS</span></span>
<span data-ttu-id="437cc-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="437cc-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="437cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="437cc-104">SYNTAX</span></span>

### <span data-ttu-id="437cc-105">S1</span><span class="sxs-lookup"><span data-stu-id="437cc-105">S1</span></span>
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

### <span data-ttu-id="437cc-106">S2</span><span class="sxs-lookup"><span data-stu-id="437cc-106">S2</span></span>
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

## <span data-ttu-id="437cc-107">說明</span><span class="sxs-lookup"><span data-stu-id="437cc-107">DESCRIPTION</span></span>
<span data-ttu-id="437cc-108">**AzWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="437cc-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="437cc-109">示例</span><span class="sxs-lookup"><span data-stu-id="437cc-109">EXAMPLES</span></span>

### <span data-ttu-id="437cc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="437cc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="437cc-111">這個命令會變更與 Slot001 相關聯的 appservice 方案（與資源群組預設-Web-WestUS 相關的 Webapp ContosoWebApp）。</span><span class="sxs-lookup"><span data-stu-id="437cc-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="437cc-112">使用連結進一步瞭解如何變更與它相關聯的 appservice 方案和限制。</span><span class="sxs-lookup"><span data-stu-id="437cc-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="437cc-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="437cc-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="437cc-114">範例2</span><span class="sxs-lookup"><span data-stu-id="437cc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="437cc-115">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="437cc-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="437cc-116">範例3</span><span class="sxs-lookup"><span data-stu-id="437cc-116">Example 3</span></span>

<span data-ttu-id="437cc-117">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="437cc-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="437cc-118"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="437cc-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="437cc-119">參數</span><span class="sxs-lookup"><span data-stu-id="437cc-119">PARAMETERS</span></span>

### <span data-ttu-id="437cc-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="437cc-120">-AlwaysOn</span></span>
<span data-ttu-id="437cc-121">確保所有時間都會載入 web 應用程式，而不是在空閒後卸載。</span><span class="sxs-lookup"><span data-stu-id="437cc-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="437cc-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="437cc-122">-AppServicePlan</span></span>
<span data-ttu-id="437cc-123">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="437cc-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="437cc-124">-AppSettings</span></span>
<span data-ttu-id="437cc-125">App 設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="437cc-125">App Settings HashTable.</span></span> <span data-ttu-id="437cc-126">現有的應用程式設定將會取代，移除任何未提供的設定。</span><span class="sxs-lookup"><span data-stu-id="437cc-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="437cc-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="437cc-127">-AsJob</span></span>
<span data-ttu-id="437cc-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="437cc-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="437cc-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="437cc-129">-AssignIdentity</span></span>
<span data-ttu-id="437cc-130">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="437cc-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="437cc-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="437cc-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="437cc-132">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="437cc-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="437cc-133">-AzureStoragePath</span></span>
<span data-ttu-id="437cc-134">[Azure 儲存空間] 可在容器的 Web App 內裝載。</span><span class="sxs-lookup"><span data-stu-id="437cc-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="437cc-135">使用 New-AzureRmWebAppAzureStoragePath 建立</span><span class="sxs-lookup"><span data-stu-id="437cc-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="437cc-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="437cc-136">-ConnectionStrings</span></span>
<span data-ttu-id="437cc-137">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="437cc-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="437cc-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="437cc-138">-ContainerImageName</span></span>
<span data-ttu-id="437cc-139">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-139">Container Image Name</span></span>

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

### <span data-ttu-id="437cc-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="437cc-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="437cc-141">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="437cc-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="437cc-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="437cc-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="437cc-143">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="437cc-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="437cc-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="437cc-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="437cc-145">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="437cc-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="437cc-146">-DefaultDocuments</span></span>
<span data-ttu-id="437cc-147">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="437cc-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="437cc-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437cc-148">-DefaultProfile</span></span>
<span data-ttu-id="437cc-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="437cc-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="437cc-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="437cc-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="437cc-151">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="437cc-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="437cc-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="437cc-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="437cc-153">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="437cc-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="437cc-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="437cc-154">-FtpsState</span></span>
<span data-ttu-id="437cc-155">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="437cc-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="437cc-156">允許的值 [AllAllowed |已停用 |FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="437cc-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="437cc-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="437cc-157">-HandlerMappings</span></span>
<span data-ttu-id="437cc-158">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="437cc-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="437cc-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="437cc-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="437cc-160">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="437cc-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="437cc-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="437cc-161">-HttpsOnly</span></span>
<span data-ttu-id="437cc-162">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="437cc-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="437cc-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="437cc-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="437cc-164">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="437cc-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="437cc-165">-MinTlsVersion</span></span>
<span data-ttu-id="437cc-166">SSL 要求所需的最小 TLS 版本。</span><span class="sxs-lookup"><span data-stu-id="437cc-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="437cc-167">允許值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="437cc-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="437cc-168">-名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-168">-Name</span></span>
<span data-ttu-id="437cc-169">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-169">WebApp Name</span></span>

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

### <span data-ttu-id="437cc-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="437cc-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="437cc-171">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="437cc-171">Net Framework Version</span></span>

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

### <span data-ttu-id="437cc-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="437cc-172">-NumberOfWorkers</span></span>
<span data-ttu-id="437cc-173">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="437cc-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="437cc-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="437cc-174">-PhpVersion</span></span>
<span data-ttu-id="437cc-175">Php 版本</span><span class="sxs-lookup"><span data-stu-id="437cc-175">Php Version</span></span>

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

### <span data-ttu-id="437cc-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="437cc-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="437cc-177">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="437cc-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="437cc-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="437cc-178">-ResourceGroupName</span></span>
<span data-ttu-id="437cc-179">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-179">Resource Group Name</span></span>

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

### <span data-ttu-id="437cc-180">-槽</span><span class="sxs-lookup"><span data-stu-id="437cc-180">-Slot</span></span>
<span data-ttu-id="437cc-181">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="437cc-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="437cc-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="437cc-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="437cc-183">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="437cc-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="437cc-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="437cc-184">-WebApp</span></span>
<span data-ttu-id="437cc-185">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="437cc-185">WebApp Object</span></span>

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

### <span data-ttu-id="437cc-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="437cc-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="437cc-187">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="437cc-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="437cc-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437cc-188">CommonParameters</span></span>
<span data-ttu-id="437cc-189">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="437cc-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437cc-190">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="437cc-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437cc-191">輸入</span><span class="sxs-lookup"><span data-stu-id="437cc-191">INPUTS</span></span>

### <span data-ttu-id="437cc-192">System.object</span><span class="sxs-lookup"><span data-stu-id="437cc-192">System.Int32</span></span>

### <span data-ttu-id="437cc-193">System.object</span><span class="sxs-lookup"><span data-stu-id="437cc-193">System.String</span></span>

### <span data-ttu-id="437cc-194">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="437cc-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="437cc-195">輸出</span><span class="sxs-lookup"><span data-stu-id="437cc-195">OUTPUTS</span></span>

### <span data-ttu-id="437cc-196">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="437cc-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="437cc-197">筆記</span><span class="sxs-lookup"><span data-stu-id="437cc-197">NOTES</span></span>

## <span data-ttu-id="437cc-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="437cc-198">RELATED LINKS</span></span>

[<span data-ttu-id="437cc-199">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="437cc-200">新-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="437cc-201">移除-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="437cc-202">重新開機-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="437cc-203">開始-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="437cc-204">停止 AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="437cc-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="437cc-205">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="437cc-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
