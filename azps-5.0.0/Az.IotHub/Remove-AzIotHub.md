---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139183"
---
# <span data-ttu-id="1571c-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="1571c-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="1571c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1571c-102">SYNOPSIS</span></span>
<span data-ttu-id="1571c-103">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="1571c-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="1571c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1571c-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1571c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1571c-105">DESCRIPTION</span></span>
<span data-ttu-id="1571c-106">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="1571c-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="1571c-107">示例</span><span class="sxs-lookup"><span data-stu-id="1571c-107">EXAMPLES</span></span>

### <span data-ttu-id="1571c-108">範例1移除 IotHub</span><span class="sxs-lookup"><span data-stu-id="1571c-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="1571c-109">移除名為 "myiothub" 的 IotHub</span><span class="sxs-lookup"><span data-stu-id="1571c-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="1571c-110">參數</span><span class="sxs-lookup"><span data-stu-id="1571c-110">PARAMETERS</span></span>

### <span data-ttu-id="1571c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1571c-111">-DefaultProfile</span></span>
<span data-ttu-id="1571c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1571c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1571c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="1571c-113">-Name</span></span>
<span data-ttu-id="1571c-114">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="1571c-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="1571c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1571c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1571c-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1571c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="1571c-117">-確認</span><span class="sxs-lookup"><span data-stu-id="1571c-117">-Confirm</span></span>
<span data-ttu-id="1571c-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1571c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1571c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1571c-119">-WhatIf</span></span>
<span data-ttu-id="1571c-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1571c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1571c-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1571c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1571c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1571c-122">CommonParameters</span></span>
<span data-ttu-id="1571c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1571c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1571c-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1571c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1571c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1571c-125">INPUTS</span></span>

### <span data-ttu-id="1571c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="1571c-126">System.String</span></span>

## <span data-ttu-id="1571c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1571c-127">OUTPUTS</span></span>

### <span data-ttu-id="1571c-128">System.void</span><span class="sxs-lookup"><span data-stu-id="1571c-128">System.Void</span></span>

## <span data-ttu-id="1571c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1571c-129">NOTES</span></span>

## <span data-ttu-id="1571c-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1571c-130">RELATED LINKS</span></span>