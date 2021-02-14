---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140798"
---
# <span data-ttu-id="f19cc-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="f19cc-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="f19cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f19cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f19cc-103">在 IoT 中樞中的目標 IoT 裝置上刪除模組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="f19cc-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f19cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f19cc-104">SYNTAX</span></span>

### <span data-ttu-id="f19cc-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f19cc-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f19cc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f19cc-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f19cc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f19cc-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f19cc-108">說明</span><span class="sxs-lookup"><span data-stu-id="f19cc-108">DESCRIPTION</span></span>
<span data-ttu-id="f19cc-109">在 IoT 中樞中的目標 IoT 裝置上刪除模組 (s) 。</span><span class="sxs-lookup"><span data-stu-id="f19cc-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="f19cc-110">示例</span><span class="sxs-lookup"><span data-stu-id="f19cc-110">EXAMPLES</span></span>

### <span data-ttu-id="f19cc-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f19cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="f19cc-112">刪除 Iot 裝置模組。</span><span class="sxs-lookup"><span data-stu-id="f19cc-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="f19cc-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f19cc-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="f19cc-114">刪除所有的 Iot 裝置模組。</span><span class="sxs-lookup"><span data-stu-id="f19cc-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="f19cc-115">參數</span><span class="sxs-lookup"><span data-stu-id="f19cc-115">PARAMETERS</span></span>

### <span data-ttu-id="f19cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19cc-116">-DefaultProfile</span></span>
<span data-ttu-id="f19cc-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f19cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19cc-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f19cc-118">-DeviceId</span></span>
<span data-ttu-id="f19cc-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19cc-119">Target Device Id.</span></span>

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

### <span data-ttu-id="f19cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f19cc-120">-InputObject</span></span>
<span data-ttu-id="f19cc-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="f19cc-121">IotHub object</span></span>

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

### <span data-ttu-id="f19cc-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f19cc-122">-IotHubName</span></span>
<span data-ttu-id="f19cc-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="f19cc-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f19cc-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="f19cc-124">-ModuleId</span></span>
<span data-ttu-id="f19cc-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f19cc-125">Target Module Id.</span></span>

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

### <span data-ttu-id="f19cc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f19cc-126">-PassThru</span></span>
<span data-ttu-id="f19cc-127">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="f19cc-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="f19cc-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f19cc-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f19cc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f19cc-129">-ResourceGroupName</span></span>
<span data-ttu-id="f19cc-130">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f19cc-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f19cc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f19cc-131">-ResourceId</span></span>
<span data-ttu-id="f19cc-132">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f19cc-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f19cc-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f19cc-133">-Confirm</span></span>
<span data-ttu-id="f19cc-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f19cc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f19cc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f19cc-135">-WhatIf</span></span>
<span data-ttu-id="f19cc-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f19cc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f19cc-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f19cc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f19cc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19cc-138">CommonParameters</span></span>
<span data-ttu-id="f19cc-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f19cc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19cc-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f19cc-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19cc-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f19cc-141">INPUTS</span></span>

### <span data-ttu-id="f19cc-142">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f19cc-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f19cc-143">System.object</span><span class="sxs-lookup"><span data-stu-id="f19cc-143">System.String</span></span>

## <span data-ttu-id="f19cc-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f19cc-144">OUTPUTS</span></span>

### <span data-ttu-id="f19cc-145">System.object</span><span class="sxs-lookup"><span data-stu-id="f19cc-145">System.Boolean</span></span>

## <span data-ttu-id="f19cc-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f19cc-146">NOTES</span></span>

## <span data-ttu-id="f19cc-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f19cc-147">RELATED LINKS</span></span>
