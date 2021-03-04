---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: f99faf1ce7420212e87c894c8f5aadeb16578334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913898"
---
# <span data-ttu-id="040a3-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="040a3-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="040a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="040a3-102">SYNOPSIS</span></span>
<span data-ttu-id="040a3-103">更新 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="040a3-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="040a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="040a3-104">SYNTAX</span></span>

### <span data-ttu-id="040a3-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="040a3-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="040a3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="040a3-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="040a3-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="040a3-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="040a3-108">描述</span><span class="sxs-lookup"><span data-stu-id="040a3-108">DESCRIPTION</span></span>
<span data-ttu-id="040a3-109">更新 IoT 中心應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="040a3-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="040a3-110">例子</span><span class="sxs-lookup"><span data-stu-id="040a3-110">EXAMPLES</span></span>

### <span data-ttu-id="040a3-111">範例 1 更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="040a3-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="040a3-112">更新現有 IoT 中心應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="040a3-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="040a3-113">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="040a3-113">Example Output:</span></span>

<span data-ttu-id="040a3-114">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： My New Custom Display Name Subdomain ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040a3-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="040a3-115">範例 2 Update Subdomain</span><span class="sxs-lookup"><span data-stu-id="040a3-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="040a3-116">更新現有 IoT 中心應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="040a3-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="040a3-117">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="040a3-117">Example Output:</span></span>

<span data-ttu-id="040a3-118">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName ： Display Name Subdomain ： new-subdomain Template ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040a3-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="040a3-119">範例 3 更新應用程式 SKU 資訊</span><span class="sxs-lookup"><span data-stu-id="040a3-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="040a3-120">更新現有 IoT 中心應用程式的 SKU。</span><span class="sxs-lookup"><span data-stu-id="040a3-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="040a3-121">輸出範例：</span><span class="sxs-lookup"><span data-stu-id="040a3-121">Example Output:</span></span>

<span data-ttu-id="040a3-122">ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： Display Name Subdomain ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040a3-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="040a3-123">參數</span><span class="sxs-lookup"><span data-stu-id="040a3-123">PARAMETERS</span></span>

### <span data-ttu-id="040a3-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="040a3-124">-AsJob</span></span>
<span data-ttu-id="040a3-125">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="040a3-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="040a3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="040a3-126">-DefaultProfile</span></span>
<span data-ttu-id="040a3-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="040a3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="040a3-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="040a3-128">-DisplayName</span></span>
<span data-ttu-id="040a3-129">Iot Central 應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="040a3-129">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="040a3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="040a3-130">-InputObject</span></span>
<span data-ttu-id="040a3-131">Iot Central Application Input Object.</span><span class="sxs-lookup"><span data-stu-id="040a3-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="040a3-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="040a3-132">-Name</span></span>
<span data-ttu-id="040a3-133">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="040a3-133">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040a3-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="040a3-134">-ResourceGroupName</span></span>
<span data-ttu-id="040a3-135">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="040a3-135">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040a3-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="040a3-136">-ResourceId</span></span>
<span data-ttu-id="040a3-137">Iot Central Application Resource Id.</span><span class="sxs-lookup"><span data-stu-id="040a3-137">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="040a3-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="040a3-138">-Sku</span></span>
<span data-ttu-id="040a3-139">IoT 中心應用程式的定價層級。</span><span class="sxs-lookup"><span data-stu-id="040a3-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="040a3-140">預設值為 ST2。</span><span class="sxs-lookup"><span data-stu-id="040a3-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="040a3-141">-Subdomain</span><span class="sxs-lookup"><span data-stu-id="040a3-141">-Subdomain</span></span>
<span data-ttu-id="040a3-142">IoT 中心應用程式的子域。</span><span class="sxs-lookup"><span data-stu-id="040a3-142">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="040a3-143">-標記</span><span class="sxs-lookup"><span data-stu-id="040a3-143">-Tag</span></span>
<span data-ttu-id="040a3-144">Iot Central Application Resource Tags.</span><span class="sxs-lookup"><span data-stu-id="040a3-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="040a3-145">-確認</span><span class="sxs-lookup"><span data-stu-id="040a3-145">-Confirm</span></span>
<span data-ttu-id="040a3-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="040a3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="040a3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="040a3-147">-WhatIf</span></span>
<span data-ttu-id="040a3-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="040a3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="040a3-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="040a3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="040a3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="040a3-150">CommonParameters</span></span>
<span data-ttu-id="040a3-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="040a3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="040a3-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="040a3-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="040a3-153">輸入</span><span class="sxs-lookup"><span data-stu-id="040a3-153">INPUTS</span></span>

### <span data-ttu-id="040a3-154">System.String</span><span class="sxs-lookup"><span data-stu-id="040a3-154">System.String</span></span>

### <span data-ttu-id="040a3-155">Microsoft.Azure.Commands.IotCentral.models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="040a3-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="040a3-156">輸出</span><span class="sxs-lookup"><span data-stu-id="040a3-156">OUTPUTS</span></span>

### <span data-ttu-id="040a3-157">Microsoft.Azure.Commands.IotCentral.models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="040a3-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="040a3-158">筆記</span><span class="sxs-lookup"><span data-stu-id="040a3-158">NOTES</span></span>

## <span data-ttu-id="040a3-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="040a3-159">RELATED LINKS</span></span>
