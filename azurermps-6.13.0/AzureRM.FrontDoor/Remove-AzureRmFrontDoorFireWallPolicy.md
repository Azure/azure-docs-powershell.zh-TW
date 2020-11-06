---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: 4dda510402b9395db24507f22d90da0f1fb6a44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443820"
---
# <span data-ttu-id="7aa9f-101">Remove-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="7aa9f-101">Remove-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="7aa9f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7aa9f-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa9f-103">移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="7aa9f-103">Remove WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7aa9f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7aa9f-104">SYNTAX</span></span>

### <span data-ttu-id="7aa9f-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7aa9f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa9f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa9f-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7aa9f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7aa9f-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7aa9f-108">說明</span><span class="sxs-lookup"><span data-stu-id="7aa9f-108">DESCRIPTION</span></span>
<span data-ttu-id="7aa9f-109">**AzureRmFrontDoor** Cmdlet 會在目前的訂閱底下移除 WAF 原則</span><span class="sxs-lookup"><span data-stu-id="7aa9f-109">The **Remove-AzureRmFrontDoor** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="7aa9f-110">示例</span><span class="sxs-lookup"><span data-stu-id="7aa9f-110">EXAMPLES</span></span>

### <span data-ttu-id="7aa9f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7aa9f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup
```

<span data-ttu-id="7aa9f-112">在 $resourceGroup 中移除稱為 $name 的 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-112">Remove the WAF policy called $name in $resourceGroup.</span></span>

### <span data-ttu-id="7aa9f-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7aa9f-113">Example 2</span></span>
```powershell
PS C:\> Get--AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Remove-AzureRmFrontDoorFireWallPolicy
```

<span data-ttu-id="7aa9f-114">移除 $resourceGroup 中的所有 WAF 原則。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-114">Remove all WAF policy in $resourceGroup.</span></span>

## <span data-ttu-id="7aa9f-115">參數</span><span class="sxs-lookup"><span data-stu-id="7aa9f-115">PARAMETERS</span></span>

### <span data-ttu-id="7aa9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa9f-116">-DefaultProfile</span></span>
<span data-ttu-id="7aa9f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7aa9f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7aa9f-118">-InputObject</span></span>
<span data-ttu-id="7aa9f-119">要刪除的 WAF 原則物件。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7aa9f-120">-Name</span></span>
<span data-ttu-id="7aa9f-121">要刪除之 WAF 原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7aa9f-122">-PassThru</span></span>
<span data-ttu-id="7aa9f-123">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="7aa9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7aa9f-125">WAF 原則所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa9f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7aa9f-126">-ResourceId</span></span>
<span data-ttu-id="7aa9f-127">要刪除之 WAF 原則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7aa9f-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="7aa9f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7aa9f-128">-Confirm</span></span>
<span data-ttu-id="7aa9f-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7aa9f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7aa9f-130">-WhatIf</span></span>
<span data-ttu-id="7aa9f-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7aa9f-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7aa9f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa9f-133">CommonParameters</span></span>
<span data-ttu-id="7aa9f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa9f-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa9f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="7aa9f-136">INPUTS</span></span>

### <span data-ttu-id="7aa9f-137">PSPolicy 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="7aa9f-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="7aa9f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="7aa9f-138">System.String</span></span>

### <span data-ttu-id="7aa9f-139">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7aa9f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7aa9f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="7aa9f-140">OUTPUTS</span></span>

### <span data-ttu-id="7aa9f-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7aa9f-141">System.Boolean</span></span>

## <span data-ttu-id="7aa9f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="7aa9f-142">NOTES</span></span>

## <span data-ttu-id="7aa9f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="7aa9f-143">RELATED LINKS</span></span>

<span data-ttu-id="7aa9f-144">[新-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
[AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="7aa9f-144">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)</span></span>
