---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d07d85aa9747982f223d45c40fc8897a0b0e3e73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916814"
---
# <span data-ttu-id="2f2b1-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="2f2b1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2b1-103">修改 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="2f2b1-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f2b1-104">SYNTAX</span></span>

### <span data-ttu-id="2f2b1-105">S1</span><span class="sxs-lookup"><span data-stu-id="2f2b1-105">S1</span></span>
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

### <span data-ttu-id="2f2b1-106">S2</span><span class="sxs-lookup"><span data-stu-id="2f2b1-106">S2</span></span>
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

## <span data-ttu-id="2f2b1-107">描述</span><span class="sxs-lookup"><span data-stu-id="2f2b1-107">DESCRIPTION</span></span>
<span data-ttu-id="2f2b1-108">**Set-AzWebApp** Cmdlet 會設定 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="2f2b1-109">例子</span><span class="sxs-lookup"><span data-stu-id="2f2b1-109">EXAMPLES</span></span>

### <span data-ttu-id="2f2b1-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f2b1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="2f2b1-111">此命令會變更與 Webapp ContosoWebApp 上與資源群組 Default-Web-WestUS 相關聯的 Appservice 方案。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="2f2b1-112">使用連結深入瞭解如何變更應用程式服務計畫和與其相關聯的限制式。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="2f2b1-113"> https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="2f2b1-113">https://docs.microsoft.com/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="2f2b1-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="2f2b1-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="2f2b1-115">此命令會針對與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp，將 Slot Slot001 的 HttpLoggingEnabled 設定為 True</span><span class="sxs-lookup"><span data-stu-id="2f2b1-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="2f2b1-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="2f2b1-116">Example 3</span></span>

<span data-ttu-id="2f2b1-117">修改 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="2f2b1-118"> (自動) </span><span class="sxs-lookup"><span data-stu-id="2f2b1-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="2f2b1-119">參數</span><span class="sxs-lookup"><span data-stu-id="2f2b1-119">PARAMETERS</span></span>

### <span data-ttu-id="2f2b1-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="2f2b1-120">-AlwaysOn</span></span>
<span data-ttu-id="2f2b1-121">確保 Web App 會一直載入，而不是閒置後卸貨。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="2f2b1-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f2b1-122">-AppServicePlan</span></span>
<span data-ttu-id="2f2b1-123">應用程式服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="2f2b1-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2f2b1-124">-AppSettings</span></span>
<span data-ttu-id="2f2b1-125">應用程式設定雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-125">App Settings HashTable.</span></span> <span data-ttu-id="2f2b1-126">現有的應用程式設定將會取代，移除未提供的任何設定。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="2f2b1-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f2b1-127">-AsJob</span></span>
<span data-ttu-id="2f2b1-128">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f2b1-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f2b1-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2f2b1-129">-AssignIdentity</span></span>
<span data-ttu-id="2f2b1-130">啟用/停用現有插槽上的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="2f2b1-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="2f2b1-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2f2b1-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="2f2b1-132">自動交換的目的地插槽名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="2f2b1-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="2f2b1-133">-AzureStoragePath</span></span>
<span data-ttu-id="2f2b1-134">要安裝在容器用 Web App 內的 Azure 儲存空間。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="2f2b1-135">使用New-AzureRmWebAppAzureStoragePath建立</span><span class="sxs-lookup"><span data-stu-id="2f2b1-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="2f2b1-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2f2b1-136">-ConnectionStrings</span></span>
<span data-ttu-id="2f2b1-137">連接字串雜湊表</span><span class="sxs-lookup"><span data-stu-id="2f2b1-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="2f2b1-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="2f2b1-138">-ContainerImageName</span></span>
<span data-ttu-id="2f2b1-139">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-139">Container Image Name</span></span>

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

### <span data-ttu-id="2f2b1-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="2f2b1-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="2f2b1-141">私人容器登錄密碼</span><span class="sxs-lookup"><span data-stu-id="2f2b1-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="2f2b1-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="2f2b1-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="2f2b1-143">Private Container Registry Server Url</span><span class="sxs-lookup"><span data-stu-id="2f2b1-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="2f2b1-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="2f2b1-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="2f2b1-145">私人容器登錄使用者名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="2f2b1-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2f2b1-146">-DefaultDocuments</span></span>
<span data-ttu-id="2f2b1-147">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="2f2b1-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="2f2b1-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2b1-148">-DefaultProfile</span></span>
<span data-ttu-id="2f2b1-149">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f2b1-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f2b1-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2f2b1-151">啟用布林值的詳細錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="2f2b1-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="2f2b1-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="2f2b1-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="2f2b1-153">啟用/停用容器連續部署網頁元件</span><span class="sxs-lookup"><span data-stu-id="2f2b1-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="2f2b1-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="2f2b1-154">-FtpsState</span></span>
<span data-ttu-id="2f2b1-155">設定應用程式的 Ftps 狀態值。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="2f2b1-156">允許的值 [全部|已停用|FtpsOnly]。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="2f2b1-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2f2b1-157">-HandlerMappings</span></span>
<span data-ttu-id="2f2b1-158">處理常式地圖 IList</span><span class="sxs-lookup"><span data-stu-id="2f2b1-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="2f2b1-159">-HTTPLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f2b1-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2f2b1-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="2f2b1-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="2f2b1-161">-HTTPsOnly</span><span class="sxs-lookup"><span data-stu-id="2f2b1-161">-HttpsOnly</span></span>
<span data-ttu-id="2f2b1-162">啟用/停用將現有插槽上的所有流量重新導向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="2f2b1-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="2f2b1-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2f2b1-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="2f2b1-164">受管理的管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="2f2b1-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2f2b1-165">-MinTlsVersion</span></span>
<span data-ttu-id="2f2b1-166">SSL 要求所需的 TLS 最低版本。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="2f2b1-167">允許的值 [1.0 | 1.1 | 1.2]。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="2f2b1-168">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-168">-Name</span></span>
<span data-ttu-id="2f2b1-169">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-169">WebApp Name</span></span>

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

### <span data-ttu-id="2f2b1-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2f2b1-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="2f2b1-171">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="2f2b1-171">Net Framework Version</span></span>

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

### <span data-ttu-id="2f2b1-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2f2b1-172">-NumberOfWorkers</span></span>
<span data-ttu-id="2f2b1-173">要配置的員工數目</span><span class="sxs-lookup"><span data-stu-id="2f2b1-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="2f2b1-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2f2b1-174">-PhpVersion</span></span>
<span data-ttu-id="2f2b1-175">Php 版本</span><span class="sxs-lookup"><span data-stu-id="2f2b1-175">Php Version</span></span>

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

### <span data-ttu-id="2f2b1-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2f2b1-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="2f2b1-177">啟用要求追蹤布林值</span><span class="sxs-lookup"><span data-stu-id="2f2b1-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="2f2b1-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f2b1-178">-ResourceGroupName</span></span>
<span data-ttu-id="2f2b1-179">資源組名</span><span class="sxs-lookup"><span data-stu-id="2f2b1-179">Resource Group Name</span></span>

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

### <span data-ttu-id="2f2b1-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-180">-Slot</span></span>
<span data-ttu-id="2f2b1-181">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="2f2b1-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2f2b1-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2f2b1-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2f2b1-183">使用 32 位的工作程式布林值</span><span class="sxs-lookup"><span data-stu-id="2f2b1-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="2f2b1-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2f2b1-184">-WebApp</span></span>
<span data-ttu-id="2f2b1-185">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2f2b1-185">WebApp Object</span></span>

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

### <span data-ttu-id="2f2b1-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2f2b1-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="2f2b1-187">啟用 Web 通訊端布林值</span><span class="sxs-lookup"><span data-stu-id="2f2b1-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="2f2b1-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2b1-188">CommonParameters</span></span>
<span data-ttu-id="2f2b1-189">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f2b1-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2b1-190">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f2b1-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2b1-191">輸入</span><span class="sxs-lookup"><span data-stu-id="2f2b1-191">INPUTS</span></span>

### <span data-ttu-id="2f2b1-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2f2b1-192">System.Int32</span></span>

### <span data-ttu-id="2f2b1-193">System.String</span><span class="sxs-lookup"><span data-stu-id="2f2b1-193">System.String</span></span>

### <span data-ttu-id="2f2b1-194">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2f2b1-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f2b1-195">輸出</span><span class="sxs-lookup"><span data-stu-id="2f2b1-195">OUTPUTS</span></span>

### <span data-ttu-id="2f2b1-196">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2f2b1-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f2b1-197">筆記</span><span class="sxs-lookup"><span data-stu-id="2f2b1-197">NOTES</span></span>

## <span data-ttu-id="2f2b1-198">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f2b1-198">RELATED LINKS</span></span>

[<span data-ttu-id="2f2b1-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2f2b1-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2f2b1-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2f2b1-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
