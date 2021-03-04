---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910490"
---
# <span data-ttu-id="0f0a0-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="0f0a0-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="0f0a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0a0-103">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="0f0a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f0a0-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f0a0-105">描述</span><span class="sxs-lookup"><span data-stu-id="0f0a0-105">DESCRIPTION</span></span>
<span data-ttu-id="0f0a0-106">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="0f0a0-107">例子</span><span class="sxs-lookup"><span data-stu-id="0f0a0-107">EXAMPLES</span></span>

### <span data-ttu-id="0f0a0-108">範例 1 移除 IotHub</span><span class="sxs-lookup"><span data-stu-id="0f0a0-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0f0a0-109">移除名為 "myiothub" 的 IotHub</span><span class="sxs-lookup"><span data-stu-id="0f0a0-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="0f0a0-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f0a0-110">PARAMETERS</span></span>

### <span data-ttu-id="0f0a0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0a0-111">-DefaultProfile</span></span>
<span data-ttu-id="0f0a0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0f0a0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f0a0-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f0a0-113">-Name</span></span>
<span data-ttu-id="0f0a0-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="0f0a0-114">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0a0-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f0a0-116">資源組名</span><span class="sxs-lookup"><span data-stu-id="0f0a0-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="0f0a0-117">-Confirm</span></span>
<span data-ttu-id="0f0a0-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f0a0-119">-WhatIf</span></span>
<span data-ttu-id="0f0a0-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f0a0-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0a0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0a0-122">CommonParameters</span></span>
<span data-ttu-id="0f0a0-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0a0-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0f0a0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0a0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="0f0a0-125">INPUTS</span></span>

### <span data-ttu-id="0f0a0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0f0a0-126">System.String</span></span>

## <span data-ttu-id="0f0a0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0f0a0-127">OUTPUTS</span></span>

### <span data-ttu-id="0f0a0-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="0f0a0-128">System.Void</span></span>

## <span data-ttu-id="0f0a0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0f0a0-129">NOTES</span></span>

## <span data-ttu-id="0f0a0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f0a0-130">RELATED LINKS</span></span>
