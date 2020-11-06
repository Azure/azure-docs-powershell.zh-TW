---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448648"
---
# <span data-ttu-id="d5a79-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="d5a79-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="d5a79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5a79-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a79-103">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="d5a79-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5a79-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5a79-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a79-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5a79-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a79-106">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="d5a79-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="d5a79-107">如果有多個同名的按鍵，清單中的第一個按鍵就會移除。</span><span class="sxs-lookup"><span data-stu-id="d5a79-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="d5a79-108">示例</span><span class="sxs-lookup"><span data-stu-id="d5a79-108">EXAMPLES</span></span>

### <span data-ttu-id="d5a79-109">範例1刪除 IotHub</span><span class="sxs-lookup"><span data-stu-id="d5a79-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="d5a79-110">從名為 "myiothub" 的 IotHub 中移除名為 iothubowner1 的索引鍵</span><span class="sxs-lookup"><span data-stu-id="d5a79-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d5a79-111">參數</span><span class="sxs-lookup"><span data-stu-id="d5a79-111">PARAMETERS</span></span>

### <span data-ttu-id="d5a79-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a79-112">-DefaultProfile</span></span>
<span data-ttu-id="d5a79-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d5a79-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d5a79-114">-KeyName</span></span>
<span data-ttu-id="d5a79-115">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="d5a79-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5a79-116">-Name</span></span>
<span data-ttu-id="d5a79-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="d5a79-117">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a79-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5a79-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d5a79-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d5a79-120">-Confirm</span></span>
<span data-ttu-id="d5a79-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d5a79-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a79-122">-WhatIf</span></span>
<span data-ttu-id="d5a79-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d5a79-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a79-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d5a79-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a79-125">CommonParameters</span></span>
<span data-ttu-id="d5a79-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5a79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a79-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5a79-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a79-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d5a79-128">INPUTS</span></span>

### <span data-ttu-id="d5a79-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d5a79-129">System.String</span></span>

## <span data-ttu-id="d5a79-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d5a79-130">OUTPUTS</span></span>

### <span data-ttu-id="d5a79-131">[System.object]。清單 ' 1 [IotHub. PSSharedAccessSignatureAuthorizationRule，IotHub，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="d5a79-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d5a79-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d5a79-132">NOTES</span></span>

## <span data-ttu-id="d5a79-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5a79-133">RELATED LINKS</span></span>

