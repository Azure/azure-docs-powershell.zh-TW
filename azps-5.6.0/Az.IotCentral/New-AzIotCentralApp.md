---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: ffae73880f66e378c7270ba5ce3645eae63064ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913905"
---
# <span data-ttu-id="35891-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="35891-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="35891-102">簡介</span><span class="sxs-lookup"><span data-stu-id="35891-102">SYNOPSIS</span></span>
<span data-ttu-id="35891-103">建立新的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="35891-104">語法</span><span class="sxs-lookup"><span data-stu-id="35891-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35891-105">描述</span><span class="sxs-lookup"><span data-stu-id="35891-105">DESCRIPTION</span></span>
<span data-ttu-id="35891-106">使用提供的屬性和中繼資料，建立新的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="35891-107">有關 IoT Central 的簡介，請參閱 https://docs.microsoft.com/azure/iot-central/ 。</span><span class="sxs-lookup"><span data-stu-id="35891-107">For an introduction to IoT Central, see https://docs.microsoft.com/azure/iot-central/.</span></span>

## <span data-ttu-id="35891-108">例子</span><span class="sxs-lookup"><span data-stu-id="35891-108">EXAMPLES</span></span>

### <span data-ttu-id="35891-109">範例 1 建立簡單的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="35891-110">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="35891-110">Example Output:</span></span>

<span data-ttu-id="35891-111">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName ： MyAppResourceName Subdomain ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35891-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="35891-112">在資源群組區域的標準定價層級 ST2 中建立 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-112">Create an IoT Central application in the standard pricing tier ST2, in the region of the resource group.</span></span>

### <span data-ttu-id="35891-113">範例 2 建立簡單的 IoT 中心應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "ST2" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="35891-114">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="35891-114">Example Output:</span></span>

<span data-ttu-id="35891-115">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： My Custom Display Name Subdomain ： MyAppSubdomain Template ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35891-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="35891-116">在 'westus' 地區使用標準定價層級 ST2 建立 IoT 中心應用程式，並依據 iotc 預設範本使用自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-116">Create an IoT Central application with the standard pricing tier ST2 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="35891-117">參數</span><span class="sxs-lookup"><span data-stu-id="35891-117">PARAMETERS</span></span>

### <span data-ttu-id="35891-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35891-118">-AsJob</span></span>
<span data-ttu-id="35891-119">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35891-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="35891-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35891-120">-DefaultProfile</span></span>
<span data-ttu-id="35891-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="35891-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35891-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35891-122">-DisplayName</span></span>
<span data-ttu-id="35891-123">IoT 中心應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="35891-124">預設值為資源名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-124">Default is resource name.</span></span>

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

### <span data-ttu-id="35891-125">-位置</span><span class="sxs-lookup"><span data-stu-id="35891-125">-Location</span></span>
<span data-ttu-id="35891-126">IoT 中心應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="35891-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="35891-127">預設值為目標資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="35891-127">Default is the location of target resource group.</span></span>

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

### <span data-ttu-id="35891-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="35891-128">-Name</span></span>
<span data-ttu-id="35891-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="35891-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35891-130">-ResourceGroupName</span></span>
<span data-ttu-id="35891-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="35891-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="35891-132">-Sku</span></span>
<span data-ttu-id="35891-133">IoT 中心應用程式的定價層級。</span><span class="sxs-lookup"><span data-stu-id="35891-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="35891-134">預設值為 ST2。</span><span class="sxs-lookup"><span data-stu-id="35891-134">Default value is ST2.</span></span>

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

### <span data-ttu-id="35891-135">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="35891-135">-Subdomain</span></span>
<span data-ttu-id="35891-136">IoT 中心 URL 的子域。</span><span class="sxs-lookup"><span data-stu-id="35891-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="35891-137">每個應用程式都必須有唯一的子域。</span><span class="sxs-lookup"><span data-stu-id="35891-137">Each application must have a unique subdomain.</span></span>

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

### <span data-ttu-id="35891-138">-標記</span><span class="sxs-lookup"><span data-stu-id="35891-138">-Tag</span></span>
<span data-ttu-id="35891-139">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="35891-139">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="35891-140">-範本</span><span class="sxs-lookup"><span data-stu-id="35891-140">-Template</span></span>
<span data-ttu-id="35891-141">IoT 中心應用程式範本名稱。</span><span class="sxs-lookup"><span data-stu-id="35891-141">IoT Central application template name.</span></span>
<span data-ttu-id="35891-142">預設值為自訂應用程式。</span><span class="sxs-lookup"><span data-stu-id="35891-142">Default is a custom application.</span></span>

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

### <span data-ttu-id="35891-143">-確認</span><span class="sxs-lookup"><span data-stu-id="35891-143">-Confirm</span></span>
<span data-ttu-id="35891-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="35891-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35891-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35891-145">-WhatIf</span></span>
<span data-ttu-id="35891-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35891-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35891-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35891-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35891-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35891-148">CommonParameters</span></span>
<span data-ttu-id="35891-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="35891-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35891-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35891-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35891-151">輸入</span><span class="sxs-lookup"><span data-stu-id="35891-151">INPUTS</span></span>

### <span data-ttu-id="35891-152">System.String</span><span class="sxs-lookup"><span data-stu-id="35891-152">System.String</span></span>

### <span data-ttu-id="35891-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="35891-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="35891-154">輸出</span><span class="sxs-lookup"><span data-stu-id="35891-154">OUTPUTS</span></span>

### <span data-ttu-id="35891-155">Microsoft.Azure.Commands.IotCentral.models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="35891-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="35891-156">筆記</span><span class="sxs-lookup"><span data-stu-id="35891-156">NOTES</span></span>

## <span data-ttu-id="35891-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="35891-157">RELATED LINKS</span></span>
