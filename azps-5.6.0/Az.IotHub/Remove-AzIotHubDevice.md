---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 15a8f9aa8ed3c0746b402b29967999d395794fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916411"
---
# <span data-ttu-id="ebced-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="ebced-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="ebced-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ebced-102">SYNOPSIS</span></span>
<span data-ttu-id="ebced-103">刪除 IoT 中樞裝置。</span><span class="sxs-lookup"><span data-stu-id="ebced-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="ebced-104">語法</span><span class="sxs-lookup"><span data-stu-id="ebced-104">SYNTAX</span></span>

### <span data-ttu-id="ebced-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ebced-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebced-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ebced-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebced-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ebced-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebced-108">描述</span><span class="sxs-lookup"><span data-stu-id="ebced-108">DESCRIPTION</span></span>
<span data-ttu-id="ebced-109">從 Iot Hub 刪除所有裝置或特定裝置。</span><span class="sxs-lookup"><span data-stu-id="ebced-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="ebced-110">例子</span><span class="sxs-lookup"><span data-stu-id="ebced-110">EXAMPLES</span></span>

### <span data-ttu-id="ebced-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ebced-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="ebced-112">刪除所有 Iot Hub 裝置。</span><span class="sxs-lookup"><span data-stu-id="ebced-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="ebced-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ebced-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="ebced-114">刪除 Iot Hub 裝置。</span><span class="sxs-lookup"><span data-stu-id="ebced-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="ebced-115">參數</span><span class="sxs-lookup"><span data-stu-id="ebced-115">PARAMETERS</span></span>

### <span data-ttu-id="ebced-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebced-116">-DefaultProfile</span></span>
<span data-ttu-id="ebced-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebced-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebced-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ebced-118">-DeviceId</span></span>
<span data-ttu-id="ebced-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="ebced-119">Target Device Id.</span></span>

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

### <span data-ttu-id="ebced-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebced-120">-InputObject</span></span>
<span data-ttu-id="ebced-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="ebced-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebced-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ebced-122">-IotHubName</span></span>
<span data-ttu-id="ebced-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="ebced-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebced-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebced-124">-PassThru</span></span>
<span data-ttu-id="ebced-125">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="ebced-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="ebced-126">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ebced-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ebced-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebced-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebced-128">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="ebced-128">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebced-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebced-129">-ResourceId</span></span>
<span data-ttu-id="ebced-130">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ebced-130">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebced-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ebced-131">-Confirm</span></span>
<span data-ttu-id="ebced-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ebced-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebced-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebced-133">-WhatIf</span></span>
<span data-ttu-id="ebced-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ebced-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebced-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ebced-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebced-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebced-136">CommonParameters</span></span>
<span data-ttu-id="ebced-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ebced-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebced-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ebced-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebced-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ebced-139">INPUTS</span></span>

### <span data-ttu-id="ebced-140">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ebced-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ebced-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ebced-141">System.String</span></span>

## <span data-ttu-id="ebced-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ebced-142">OUTPUTS</span></span>

### <span data-ttu-id="ebced-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebced-143">System.Boolean</span></span>

## <span data-ttu-id="ebced-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ebced-144">NOTES</span></span>

## <span data-ttu-id="ebced-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebced-145">RELATED LINKS</span></span>
