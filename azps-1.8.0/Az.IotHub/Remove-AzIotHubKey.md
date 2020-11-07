---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787490"
---
# <span data-ttu-id="62abe-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="62abe-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="62abe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62abe-102">SYNOPSIS</span></span>
<span data-ttu-id="62abe-103">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="62abe-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="62abe-104">句法</span><span class="sxs-lookup"><span data-stu-id="62abe-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62abe-105">說明</span><span class="sxs-lookup"><span data-stu-id="62abe-105">DESCRIPTION</span></span>
<span data-ttu-id="62abe-106">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="62abe-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="62abe-107">如果有多個同名的按鍵，清單中的第一個按鍵就會移除。</span><span class="sxs-lookup"><span data-stu-id="62abe-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="62abe-108">示例</span><span class="sxs-lookup"><span data-stu-id="62abe-108">EXAMPLES</span></span>

### <span data-ttu-id="62abe-109">範例1刪除 IotHub</span><span class="sxs-lookup"><span data-stu-id="62abe-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="62abe-110">從名為 "myiothub" 的 IotHub 中移除名為 iothubowner1 的索引鍵</span><span class="sxs-lookup"><span data-stu-id="62abe-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="62abe-111">參數</span><span class="sxs-lookup"><span data-stu-id="62abe-111">PARAMETERS</span></span>

### <span data-ttu-id="62abe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62abe-112">-DefaultProfile</span></span>
<span data-ttu-id="62abe-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="62abe-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62abe-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="62abe-114">-KeyName</span></span>
<span data-ttu-id="62abe-115">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="62abe-115">Name of the Key</span></span>

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

### <span data-ttu-id="62abe-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="62abe-116">-Name</span></span>
<span data-ttu-id="62abe-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="62abe-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="62abe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62abe-118">-ResourceGroupName</span></span>
<span data-ttu-id="62abe-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="62abe-119">Resource Group Name</span></span>

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

### <span data-ttu-id="62abe-120">-確認</span><span class="sxs-lookup"><span data-stu-id="62abe-120">-Confirm</span></span>
<span data-ttu-id="62abe-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62abe-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62abe-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62abe-122">-WhatIf</span></span>
<span data-ttu-id="62abe-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62abe-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62abe-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62abe-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62abe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62abe-125">CommonParameters</span></span>
<span data-ttu-id="62abe-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62abe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62abe-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62abe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62abe-128">輸入</span><span class="sxs-lookup"><span data-stu-id="62abe-128">INPUTS</span></span>

### <span data-ttu-id="62abe-129">System.object</span><span class="sxs-lookup"><span data-stu-id="62abe-129">System.String</span></span>

## <span data-ttu-id="62abe-130">輸出</span><span class="sxs-lookup"><span data-stu-id="62abe-130">OUTPUTS</span></span>

### <span data-ttu-id="62abe-131">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="62abe-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="62abe-132">筆記</span><span class="sxs-lookup"><span data-stu-id="62abe-132">NOTES</span></span>

## <span data-ttu-id="62abe-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="62abe-133">RELATED LINKS</span></span>
