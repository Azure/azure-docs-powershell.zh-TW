---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 1529b7b70ec25a7ee8f4b047e28fe77efaf92351
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787505"
---
# <span data-ttu-id="c6268-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="c6268-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="c6268-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6268-102">SYNOPSIS</span></span>
<span data-ttu-id="c6268-103">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="c6268-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="c6268-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6268-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6268-105">說明</span><span class="sxs-lookup"><span data-stu-id="c6268-105">DESCRIPTION</span></span>
<span data-ttu-id="c6268-106">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="c6268-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="c6268-107">示例</span><span class="sxs-lookup"><span data-stu-id="c6268-107">EXAMPLES</span></span>

### <span data-ttu-id="c6268-108">範例1移除 IotHub</span><span class="sxs-lookup"><span data-stu-id="c6268-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="c6268-109">移除名為 "myiothub" 的 IotHub</span><span class="sxs-lookup"><span data-stu-id="c6268-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="c6268-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6268-110">PARAMETERS</span></span>

### <span data-ttu-id="c6268-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6268-111">-DefaultProfile</span></span>
<span data-ttu-id="c6268-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c6268-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6268-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6268-113">-Name</span></span>
<span data-ttu-id="c6268-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c6268-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="c6268-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6268-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6268-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c6268-116">Resource Group Name</span></span>

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

### <span data-ttu-id="c6268-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c6268-117">-Confirm</span></span>
<span data-ttu-id="c6268-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6268-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6268-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6268-119">-WhatIf</span></span>
<span data-ttu-id="c6268-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6268-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6268-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6268-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6268-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6268-122">CommonParameters</span></span>
<span data-ttu-id="c6268-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6268-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6268-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c6268-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6268-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c6268-125">INPUTS</span></span>

### <span data-ttu-id="c6268-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c6268-126">System.String</span></span>

## <span data-ttu-id="c6268-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c6268-127">OUTPUTS</span></span>

### <span data-ttu-id="c6268-128">System.void</span><span class="sxs-lookup"><span data-stu-id="c6268-128">System.Void</span></span>

## <span data-ttu-id="c6268-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c6268-129">NOTES</span></span>

## <span data-ttu-id="c6268-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6268-130">RELATED LINKS</span></span>
