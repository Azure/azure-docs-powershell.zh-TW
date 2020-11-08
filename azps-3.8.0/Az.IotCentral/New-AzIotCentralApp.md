---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: af622bbbed98a897df1774303f1417723ebfb32c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796913"
---
# <span data-ttu-id="efc84-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="efc84-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="efc84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efc84-102">SYNOPSIS</span></span>
<span data-ttu-id="efc84-103">建立新的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="efc84-104">句法</span><span class="sxs-lookup"><span data-stu-id="efc84-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc84-105">說明</span><span class="sxs-lookup"><span data-stu-id="efc84-105">DESCRIPTION</span></span>
<span data-ttu-id="efc84-106">使用提供的屬性和中繼資料建立新的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="efc84-107">如需 IoT 中央簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-central/ 。</span><span class="sxs-lookup"><span data-stu-id="efc84-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="efc84-108">示例</span><span class="sxs-lookup"><span data-stu-id="efc84-108">EXAMPLES</span></span>

### <span data-ttu-id="efc84-109">範例1建立簡單的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="efc84-110">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="efc84-110">Example Output:</span></span>

<span data-ttu-id="efc84-111">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：，. westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]： []： IoTCentral 範本： [ iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx] Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx PSIotCentralAppSkuInfo： [MyAppResourceName]</span><span class="sxs-lookup"><span data-stu-id="efc84-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="efc84-112">在 [資源] 群組中的 [標準定價層 ST2] 中建立 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="efc84-113">範例2建立簡單的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="efc84-114">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="efc84-114">Example Output:</span></span>

<span data-ttu-id="efc84-115">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：的。 westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName]：我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain。</span><span class="sxs-lookup"><span data-stu-id="efc84-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="efc84-116">根據 iotc 預設範本，在具有自訂顯示名稱的 [westus] 區域中建立具有標準定價層 ST2 的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="efc84-117">參數</span><span class="sxs-lookup"><span data-stu-id="efc84-117">PARAMETERS</span></span>

### <span data-ttu-id="efc84-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efc84-118">-AsJob</span></span>
<span data-ttu-id="efc84-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="efc84-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="efc84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc84-120">-DefaultProfile</span></span>
<span data-ttu-id="efc84-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efc84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc84-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="efc84-122">-DisplayName</span></span>
<span data-ttu-id="efc84-123">IoT 中央應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="efc84-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="efc84-124">預設值為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="efc84-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-125">-位置</span><span class="sxs-lookup"><span data-stu-id="efc84-125">-Location</span></span>
<span data-ttu-id="efc84-126">您的 IoT 中央應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="efc84-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="efc84-127">[預設值] 是 [目標資源] 群組的位置。</span><span class="sxs-lookup"><span data-stu-id="efc84-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="efc84-128">-Name</span></span>
<span data-ttu-id="efc84-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="efc84-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc84-130">-ResourceGroupName</span></span>
<span data-ttu-id="efc84-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efc84-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="efc84-132">-Sku</span></span>
<span data-ttu-id="efc84-133">IoT 中心應用程式的定價層。</span><span class="sxs-lookup"><span data-stu-id="efc84-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="efc84-134">預設值為 ST2。</span><span class="sxs-lookup"><span data-stu-id="efc84-134">Default value is ST2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-135">-子域</span><span class="sxs-lookup"><span data-stu-id="efc84-135">-Subdomain</span></span>
<span data-ttu-id="efc84-136">IoT 中央 URL 的子域。</span><span class="sxs-lookup"><span data-stu-id="efc84-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="efc84-137">每個應用程式都必須有一個唯一的子域。</span><span class="sxs-lookup"><span data-stu-id="efc84-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="efc84-138">-Tag</span></span>
<span data-ttu-id="efc84-139">Iot 中心應用程式資源標記。</span><span class="sxs-lookup"><span data-stu-id="efc84-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-140">-範本</span><span class="sxs-lookup"><span data-stu-id="efc84-140">-Template</span></span>
<span data-ttu-id="efc84-141">IoT 中央應用程式範本名稱。</span><span class="sxs-lookup"><span data-stu-id="efc84-141">IoT Central application template name.</span></span>
<span data-ttu-id="efc84-142">預設值是自訂的應用程式。</span><span class="sxs-lookup"><span data-stu-id="efc84-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-143">-確認</span><span class="sxs-lookup"><span data-stu-id="efc84-143">-Confirm</span></span>
<span data-ttu-id="efc84-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efc84-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc84-145">-WhatIf</span></span>
<span data-ttu-id="efc84-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efc84-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc84-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efc84-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc84-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc84-148">CommonParameters</span></span>
<span data-ttu-id="efc84-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efc84-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc84-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efc84-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc84-151">輸入</span><span class="sxs-lookup"><span data-stu-id="efc84-151">INPUTS</span></span>

### <span data-ttu-id="efc84-152">System.object</span><span class="sxs-lookup"><span data-stu-id="efc84-152">System.String</span></span>

### <span data-ttu-id="efc84-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="efc84-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="efc84-154">輸出</span><span class="sxs-lookup"><span data-stu-id="efc84-154">OUTPUTS</span></span>

### <span data-ttu-id="efc84-155">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="efc84-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="efc84-156">筆記</span><span class="sxs-lookup"><span data-stu-id="efc84-156">NOTES</span></span>

## <span data-ttu-id="efc84-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="efc84-157">RELATED LINKS</span></span>