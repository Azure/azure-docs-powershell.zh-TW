---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449649"
---
# <span data-ttu-id="9f0f1-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="9f0f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9f0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0f1-103">修改 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f0f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="9f0f1-104">SYNTAX</span></span>

### <span data-ttu-id="9f0f1-105">S1</span><span class="sxs-lookup"><span data-stu-id="9f0f1-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f0f1-106">S2</span><span class="sxs-lookup"><span data-stu-id="9f0f1-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f0f1-107">說明</span><span class="sxs-lookup"><span data-stu-id="9f0f1-107">DESCRIPTION</span></span>
<span data-ttu-id="9f0f1-108">**AzureRmWebApp** Cmdlet 會設定 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="9f0f1-109">示例</span><span class="sxs-lookup"><span data-stu-id="9f0f1-109">EXAMPLES</span></span>

### <span data-ttu-id="9f0f1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9f0f1-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="9f0f1-111">這個命令會針對與資源群組預設-WestUS 相關的 Web App ContosoWebApp，將 HttpLoggingEnabled 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="9f0f1-112">參數</span><span class="sxs-lookup"><span data-stu-id="9f0f1-112">PARAMETERS</span></span>

### <span data-ttu-id="9f0f1-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f0f1-113">-AppServicePlan</span></span>
<span data-ttu-id="9f0f1-114">App 服務方案名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="9f0f1-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="9f0f1-115">-AppSettings</span></span>
<span data-ttu-id="9f0f1-116">App 設定 HashTable</span><span class="sxs-lookup"><span data-stu-id="9f0f1-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="9f0f1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f0f1-117">-AsJob</span></span>
<span data-ttu-id="9f0f1-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9f0f1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f0f1-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9f0f1-119">-AssignIdentity</span></span>
<span data-ttu-id="9f0f1-120">啟用/停用現有槽中的 MSI [預覽]</span><span class="sxs-lookup"><span data-stu-id="9f0f1-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="9f0f1-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="9f0f1-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="9f0f1-122">自動交換的目的地槽名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="9f0f1-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9f0f1-123">-ConnectionStrings</span></span>
<span data-ttu-id="9f0f1-124">連接字串 HashTable</span><span class="sxs-lookup"><span data-stu-id="9f0f1-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="9f0f1-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="9f0f1-125">-ContainerImageName</span></span>
<span data-ttu-id="9f0f1-126">容器圖像名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-126">Container Image Name</span></span>

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

### <span data-ttu-id="9f0f1-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="9f0f1-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="9f0f1-128">私人容器註冊密碼</span><span class="sxs-lookup"><span data-stu-id="9f0f1-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="9f0f1-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="9f0f1-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="9f0f1-130">私人容器登錄伺服器 Url</span><span class="sxs-lookup"><span data-stu-id="9f0f1-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="9f0f1-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="9f0f1-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="9f0f1-132">私人容器註冊使用者名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="9f0f1-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="9f0f1-133">-DefaultDocuments</span></span>
<span data-ttu-id="9f0f1-134">預設檔字串陣列</span><span class="sxs-lookup"><span data-stu-id="9f0f1-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="9f0f1-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0f1-135">-DefaultProfile</span></span>
<span data-ttu-id="9f0f1-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f0f1-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9f0f1-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="9f0f1-138">詳細的錯誤記錄啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="9f0f1-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="9f0f1-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="9f0f1-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="9f0f1-140">啟用/停用容器連續部署 webhook</span><span class="sxs-lookup"><span data-stu-id="9f0f1-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="9f0f1-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="9f0f1-141">-HandlerMappings</span></span>
<span data-ttu-id="9f0f1-142">處理常式映射 IList</span><span class="sxs-lookup"><span data-stu-id="9f0f1-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="9f0f1-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="9f0f1-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="9f0f1-144">HttpLoggingEnabled 布林值</span><span class="sxs-lookup"><span data-stu-id="9f0f1-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="9f0f1-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="9f0f1-145">-HttpsOnly</span></span>
<span data-ttu-id="9f0f1-146">啟用/停用現有槽中的所有流量重定向至 HTTPS</span><span class="sxs-lookup"><span data-stu-id="9f0f1-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="9f0f1-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="9f0f1-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="9f0f1-148">Managed 管線模式名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="9f0f1-149">-名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-149">-Name</span></span>
<span data-ttu-id="9f0f1-150">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-150">WebApp Name</span></span>

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

### <span data-ttu-id="9f0f1-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="9f0f1-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="9f0f1-152">Net Framework 版本</span><span class="sxs-lookup"><span data-stu-id="9f0f1-152">Net Framework Version</span></span>

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

### <span data-ttu-id="9f0f1-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="9f0f1-153">-NumberOfWorkers</span></span>
<span data-ttu-id="9f0f1-154">要配置的工作分派人數</span><span class="sxs-lookup"><span data-stu-id="9f0f1-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="9f0f1-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="9f0f1-155">-PhpVersion</span></span>
<span data-ttu-id="9f0f1-156">Php 版本</span><span class="sxs-lookup"><span data-stu-id="9f0f1-156">Php Version</span></span>

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

### <span data-ttu-id="9f0f1-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="9f0f1-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="9f0f1-158">要求追蹤已啟用的布林值</span><span class="sxs-lookup"><span data-stu-id="9f0f1-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="9f0f1-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0f1-159">-ResourceGroupName</span></span>
<span data-ttu-id="9f0f1-160">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-160">Resource Group Name</span></span>

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

### <span data-ttu-id="9f0f1-161">-槽</span><span class="sxs-lookup"><span data-stu-id="9f0f1-161">-Slot</span></span>
<span data-ttu-id="9f0f1-162">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="9f0f1-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="9f0f1-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="9f0f1-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="9f0f1-164">使用32位的輔助進程布林值</span><span class="sxs-lookup"><span data-stu-id="9f0f1-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="9f0f1-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9f0f1-165">-WebApp</span></span>
<span data-ttu-id="9f0f1-166">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="9f0f1-166">WebApp Object</span></span>

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

### <span data-ttu-id="9f0f1-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="9f0f1-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="9f0f1-168">啟用網頁通訊端的布林值</span><span class="sxs-lookup"><span data-stu-id="9f0f1-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="9f0f1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0f1-169">CommonParameters</span></span>
<span data-ttu-id="9f0f1-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0f1-171">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9f0f1-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0f1-172">輸入</span><span class="sxs-lookup"><span data-stu-id="9f0f1-172">INPUTS</span></span>

### <span data-ttu-id="9f0f1-173">System.object</span><span class="sxs-lookup"><span data-stu-id="9f0f1-173">System.Int32</span></span>
<span data-ttu-id="9f0f1-174">參數： NumberOfWorkers (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9f0f1-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="9f0f1-175">System.object</span><span class="sxs-lookup"><span data-stu-id="9f0f1-175">System.String</span></span>

### <span data-ttu-id="9f0f1-176">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9f0f1-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="9f0f1-177">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="9f0f1-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="9f0f1-178">輸出</span><span class="sxs-lookup"><span data-stu-id="9f0f1-178">OUTPUTS</span></span>

### <span data-ttu-id="9f0f1-179">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="9f0f1-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="9f0f1-180">筆記</span><span class="sxs-lookup"><span data-stu-id="9f0f1-180">NOTES</span></span>

## <span data-ttu-id="9f0f1-181">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f0f1-181">RELATED LINKS</span></span>

[<span data-ttu-id="9f0f1-182">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-183">新-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-184">移除-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-185">重新開機-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-186">開始-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-187">停止 AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9f0f1-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="9f0f1-188">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="9f0f1-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
