---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: b7b89f239949f6a61e3388b0f5cb794cd4ad0c53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915470"
---
# <span data-ttu-id="adb91-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="adb91-101">Update-AzIotHub</span></span>

## <span data-ttu-id="adb91-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adb91-102">SYNOPSIS</span></span>
<span data-ttu-id="adb91-103">更新 Azure IoT 中樞。</span><span class="sxs-lookup"><span data-stu-id="adb91-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="adb91-104">語法</span><span class="sxs-lookup"><span data-stu-id="adb91-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adb91-105">描述</span><span class="sxs-lookup"><span data-stu-id="adb91-105">DESCRIPTION</span></span>
<span data-ttu-id="adb91-106">您可以更新 IotHub 的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="adb91-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="adb91-107">例子</span><span class="sxs-lookup"><span data-stu-id="adb91-107">EXAMPLES</span></span>

### <span data-ttu-id="adb91-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="adb91-108">Example 1</span></span>
```
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -Tag $updatedTag

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiothub
Name           : myiothub
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[key0, value0]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="adb91-109">更新 IoT 中樞的標記。</span><span class="sxs-lookup"><span data-stu-id="adb91-109">Update tags of an IoT Hub.</span></span>

## <span data-ttu-id="adb91-110">參數</span><span class="sxs-lookup"><span data-stu-id="adb91-110">PARAMETERS</span></span>

### <span data-ttu-id="adb91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb91-111">-DefaultProfile</span></span>
<span data-ttu-id="adb91-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="adb91-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb91-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="adb91-113">-Name</span></span>
<span data-ttu-id="adb91-114">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="adb91-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb91-115">-重設</span><span class="sxs-lookup"><span data-stu-id="adb91-115">-Reset</span></span>
<span data-ttu-id="adb91-116">重設 IoTHub 標記</span><span class="sxs-lookup"><span data-stu-id="adb91-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="adb91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adb91-117">-ResourceGroupName</span></span>
<span data-ttu-id="adb91-118">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="adb91-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adb91-119">-標記</span><span class="sxs-lookup"><span data-stu-id="adb91-119">-Tag</span></span>
<span data-ttu-id="adb91-120">IoTHub 標記集合</span><span class="sxs-lookup"><span data-stu-id="adb91-120">IoTHub Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adb91-121">-確認</span><span class="sxs-lookup"><span data-stu-id="adb91-121">-Confirm</span></span>
<span data-ttu-id="adb91-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="adb91-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adb91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adb91-123">-WhatIf</span></span>
<span data-ttu-id="adb91-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adb91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adb91-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adb91-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adb91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb91-126">CommonParameters</span></span>
<span data-ttu-id="adb91-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adb91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb91-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="adb91-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb91-129">輸入</span><span class="sxs-lookup"><span data-stu-id="adb91-129">INPUTS</span></span>

### <span data-ttu-id="adb91-130">System.String</span><span class="sxs-lookup"><span data-stu-id="adb91-130">System.String</span></span>

## <span data-ttu-id="adb91-131">輸出</span><span class="sxs-lookup"><span data-stu-id="adb91-131">OUTPUTS</span></span>

### <span data-ttu-id="adb91-132">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="adb91-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="adb91-133">筆記</span><span class="sxs-lookup"><span data-stu-id="adb91-133">NOTES</span></span>

## <span data-ttu-id="adb91-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="adb91-134">RELATED LINKS</span></span>
