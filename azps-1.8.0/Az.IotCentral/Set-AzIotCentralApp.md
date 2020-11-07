---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787586"
---
# <span data-ttu-id="474c3-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="474c3-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="474c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="474c3-102">SYNOPSIS</span></span>
<span data-ttu-id="474c3-103">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="474c3-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="474c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="474c3-104">SYNTAX</span></span>

### <span data-ttu-id="474c3-105">ResourceIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="474c3-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474c3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="474c3-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="474c3-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="474c3-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="474c3-108">說明</span><span class="sxs-lookup"><span data-stu-id="474c3-108">DESCRIPTION</span></span>
<span data-ttu-id="474c3-109">更新 IoT 中央應用程式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="474c3-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="474c3-110">示例</span><span class="sxs-lookup"><span data-stu-id="474c3-110">EXAMPLES</span></span>

### <span data-ttu-id="474c3-111">範例1更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="474c3-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="474c3-112">更新現有 IoT 中央應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="474c3-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="474c3-113">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="474c3-113">Example Output:</span></span>

<span data-ttu-id="474c3-114">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：：的。 westus ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX]-xxxx xxxx：我的新自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 SubscriptionId： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain</span><span class="sxs-lookup"><span data-stu-id="474c3-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="474c3-115">範例2更新子域</span><span class="sxs-lookup"><span data-stu-id="474c3-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="474c3-116">更新現有 IoT 中央應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="474c3-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="474c3-117">範例輸出：</span><span class="sxs-lookup"><span data-stu-id="474c3-117">Example Output:</span></span>

<span data-ttu-id="474c3-118">ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型：/IoTCentral 位置： IoTApps 標記： Sku：.. Westus. IoTCentral ApplicationId： [XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX 名稱] 子 DisplayName：顯示名稱子域：新的子域範本： SubscriptionId： [xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx]： [ iotc-default@1.0.0 PSIotCentralAppSkuInfo]</span><span class="sxs-lookup"><span data-stu-id="474c3-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="474c3-119">參數</span><span class="sxs-lookup"><span data-stu-id="474c3-119">PARAMETERS</span></span>

### <span data-ttu-id="474c3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="474c3-120">-AsJob</span></span>
<span data-ttu-id="474c3-121">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="474c3-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="474c3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474c3-122">-DefaultProfile</span></span>
<span data-ttu-id="474c3-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="474c3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="474c3-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="474c3-124">-DisplayName</span></span>
<span data-ttu-id="474c3-125">Iot 中央應用程式的自訂顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="474c3-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="474c3-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="474c3-126">-InputObject</span></span>
<span data-ttu-id="474c3-127">Iot 中央應用程式輸入物件。</span><span class="sxs-lookup"><span data-stu-id="474c3-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="474c3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="474c3-128">-Name</span></span>
<span data-ttu-id="474c3-129">Iot 中心應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="474c3-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="474c3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="474c3-130">-ResourceGroupName</span></span>
<span data-ttu-id="474c3-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="474c3-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="474c3-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="474c3-132">-ResourceId</span></span>
<span data-ttu-id="474c3-133">Iot 中心應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="474c3-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="474c3-134">-子域</span><span class="sxs-lookup"><span data-stu-id="474c3-134">-Subdomain</span></span>
<span data-ttu-id="474c3-135">IoT 中央應用程式的子域。</span><span class="sxs-lookup"><span data-stu-id="474c3-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="474c3-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="474c3-136">-Tag</span></span>
<span data-ttu-id="474c3-137">Iot 中心應用程式資源標記。</span><span class="sxs-lookup"><span data-stu-id="474c3-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="474c3-138">-確認</span><span class="sxs-lookup"><span data-stu-id="474c3-138">-Confirm</span></span>
<span data-ttu-id="474c3-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="474c3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="474c3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="474c3-140">-WhatIf</span></span>
<span data-ttu-id="474c3-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="474c3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="474c3-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="474c3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="474c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474c3-143">CommonParameters</span></span>
<span data-ttu-id="474c3-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="474c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474c3-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="474c3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474c3-146">輸入</span><span class="sxs-lookup"><span data-stu-id="474c3-146">INPUTS</span></span>

### <span data-ttu-id="474c3-147">System.object</span><span class="sxs-lookup"><span data-stu-id="474c3-147">System.String</span></span>

### <span data-ttu-id="474c3-148">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="474c3-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="474c3-149">輸出</span><span class="sxs-lookup"><span data-stu-id="474c3-149">OUTPUTS</span></span>

### <span data-ttu-id="474c3-150">PSIotCentralApp 中的 IotCentral。</span><span class="sxs-lookup"><span data-stu-id="474c3-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="474c3-151">筆記</span><span class="sxs-lookup"><span data-stu-id="474c3-151">NOTES</span></span>

## <span data-ttu-id="474c3-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="474c3-152">RELATED LINKS</span></span>
