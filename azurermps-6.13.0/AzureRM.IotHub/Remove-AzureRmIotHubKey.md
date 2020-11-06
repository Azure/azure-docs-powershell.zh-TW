---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446992"
---
# <span data-ttu-id="24dc7-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="24dc7-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="24dc7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="24dc7-103">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="24dc7-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24dc7-104">句法</span><span class="sxs-lookup"><span data-stu-id="24dc7-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24dc7-105">說明</span><span class="sxs-lookup"><span data-stu-id="24dc7-105">DESCRIPTION</span></span>
<span data-ttu-id="24dc7-106">移除 IotHub 鍵。</span><span class="sxs-lookup"><span data-stu-id="24dc7-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="24dc7-107">如果有多個同名的按鍵，清單中的第一個按鍵就會移除。</span><span class="sxs-lookup"><span data-stu-id="24dc7-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="24dc7-108">示例</span><span class="sxs-lookup"><span data-stu-id="24dc7-108">EXAMPLES</span></span>

### <span data-ttu-id="24dc7-109">範例1刪除 IotHub</span><span class="sxs-lookup"><span data-stu-id="24dc7-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="24dc7-110">從名為 "myiothub" 的 IotHub 中移除名為 iothubowner1 的索引鍵</span><span class="sxs-lookup"><span data-stu-id="24dc7-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="24dc7-111">參數</span><span class="sxs-lookup"><span data-stu-id="24dc7-111">PARAMETERS</span></span>

### <span data-ttu-id="24dc7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24dc7-112">-DefaultProfile</span></span>
<span data-ttu-id="24dc7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="24dc7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24dc7-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="24dc7-114">-KeyName</span></span>
<span data-ttu-id="24dc7-115">索引鍵的名稱</span><span class="sxs-lookup"><span data-stu-id="24dc7-115">Name of the Key</span></span>

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

### <span data-ttu-id="24dc7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="24dc7-116">-Name</span></span>
<span data-ttu-id="24dc7-117">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="24dc7-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="24dc7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24dc7-118">-ResourceGroupName</span></span>
<span data-ttu-id="24dc7-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="24dc7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="24dc7-120">-確認</span><span class="sxs-lookup"><span data-stu-id="24dc7-120">-Confirm</span></span>
<span data-ttu-id="24dc7-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24dc7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24dc7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24dc7-122">-WhatIf</span></span>
<span data-ttu-id="24dc7-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24dc7-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24dc7-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24dc7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24dc7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24dc7-125">CommonParameters</span></span>
<span data-ttu-id="24dc7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24dc7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24dc7-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24dc7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24dc7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="24dc7-128">INPUTS</span></span>

### <span data-ttu-id="24dc7-129">System.object</span><span class="sxs-lookup"><span data-stu-id="24dc7-129">System.String</span></span>

## <span data-ttu-id="24dc7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="24dc7-130">OUTPUTS</span></span>

### <span data-ttu-id="24dc7-131">PSSharedAccessSignatureAuthorizationRule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="24dc7-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="24dc7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="24dc7-132">NOTES</span></span>

## <span data-ttu-id="24dc7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="24dc7-133">RELATED LINKS</span></span>
