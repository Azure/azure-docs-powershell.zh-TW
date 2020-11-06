---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/new-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/New-AzureRmIotCentralApp.md
ms.openlocfilehash: d0bb10324c1a97b6228a26a7ab079edb4845d48a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457032"
---
# <span data-ttu-id="9ee6f-101">New-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="9ee6f-101">New-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="9ee6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ee6f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ee6f-103">建立新的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-103">Creates a new IoT Central Application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ee6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ee6f-104">SYNTAX</span></span>

```
New-AzureRmIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ee6f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ee6f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ee6f-106">使用提供的屬性和中繼資料建立新的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="9ee6f-107">如需 IoT 中央簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-central/ 。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="9ee6f-108">示例</span><span class="sxs-lookup"><span data-stu-id="9ee6f-108">EXAMPLES</span></span>

### <span data-ttu-id="9ee6f-109">範例1建立簡單的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="9ee6f-110">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="9ee6f-110">Example Output:</span></span>

<span data-ttu-id="9ee6f-111">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：，. westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]： []： IoTCentral 範本： [ iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx] Xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx PSIotCentralAppSkuInfo： [MyAppResourceName]</span><span class="sxs-lookup"><span data-stu-id="9ee6f-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="9ee6f-112">在 [資源] 群組的區域中，在標準定價層 S1 中建立 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="9ee6f-113">範例2建立簡單的 IoT 中央應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="9ee6f-114">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="9ee6f-114">Example Output:</span></span>

<span data-ttu-id="9ee6f-115">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：的。 westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName]：我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="9ee6f-116">使用 [westus] 區域中的標準定價層 S1 建立包含自訂顯示名稱的 IoT 中心應用程式（根據 iotc 預設範本）。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="9ee6f-117">參數</span><span class="sxs-lookup"><span data-stu-id="9ee6f-117">PARAMETERS</span></span>

### <span data-ttu-id="9ee6f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ee6f-118">-AsJob</span></span>
<span data-ttu-id="9ee6f-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ee6f-120">-DefaultProfile</span></span>
<span data-ttu-id="9ee6f-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9ee6f-122">-DisplayName</span></span>
<span data-ttu-id="9ee6f-123">IoT 中央應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="9ee6f-124">預設值為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-124">Default is resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-125">-位置</span><span class="sxs-lookup"><span data-stu-id="9ee6f-125">-Location</span></span>
<span data-ttu-id="9ee6f-126">您的 IoT 中央應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="9ee6f-127">[預設值] 是 [目標資源] 群組的位置。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-127">Default is the location of target resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ee6f-128">-Name</span></span>
<span data-ttu-id="9ee6f-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ee6f-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ee6f-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="9ee6f-132">-Sku</span></span>
<span data-ttu-id="9ee6f-133">IoT 中心應用程式的定價層。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="9ee6f-134">預設值為 S1。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-134">Default value is S1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-135">-子域</span><span class="sxs-lookup"><span data-stu-id="9ee6f-135">-Subdomain</span></span>
<span data-ttu-id="9ee6f-136">IoT 中央 URL 的子域。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="9ee6f-137">每個應用程式都必須有一個唯一的子域。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="9ee6f-138">-Tag</span></span>
<span data-ttu-id="9ee6f-139">Iot 中心應用程式資源標記。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-140">-範本</span><span class="sxs-lookup"><span data-stu-id="9ee6f-140">-Template</span></span>
<span data-ttu-id="9ee6f-141">IoT 中央應用程式範本名稱。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-141">IoT Central application template name.</span></span>
<span data-ttu-id="9ee6f-142">預設值是自訂的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-142">Default is a custom application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-143">-確認</span><span class="sxs-lookup"><span data-stu-id="9ee6f-143">-Confirm</span></span>
<span data-ttu-id="9ee6f-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ee6f-145">-WhatIf</span></span>
<span data-ttu-id="9ee6f-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ee6f-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ee6f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ee6f-148">CommonParameters</span></span>
<span data-ttu-id="9ee6f-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ee6f-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ee6f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="9ee6f-151">INPUTS</span></span>

### <span data-ttu-id="9ee6f-152">System.object</span><span class="sxs-lookup"><span data-stu-id="9ee6f-152">System.String</span></span>
### <span data-ttu-id="9ee6f-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9ee6f-153">System.Collections.Hashtable</span></span>
## <span data-ttu-id="9ee6f-154">輸出</span><span class="sxs-lookup"><span data-stu-id="9ee6f-154">OUTPUTS</span></span>

### <span data-ttu-id="9ee6f-155">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="9ee6f-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="9ee6f-156">筆記</span><span class="sxs-lookup"><span data-stu-id="9ee6f-156">NOTES</span></span>

## <span data-ttu-id="9ee6f-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ee6f-157">RELATED LINKS</span></span>
