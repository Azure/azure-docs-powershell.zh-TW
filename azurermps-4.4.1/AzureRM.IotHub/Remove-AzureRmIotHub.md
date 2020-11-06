---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453476"
---
# <span data-ttu-id="5eb15-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="5eb15-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="5eb15-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5eb15-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb15-103">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="5eb15-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5eb15-104">句法</span><span class="sxs-lookup"><span data-stu-id="5eb15-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb15-105">說明</span><span class="sxs-lookup"><span data-stu-id="5eb15-105">DESCRIPTION</span></span>
<span data-ttu-id="5eb15-106">刪除 IotHub。</span><span class="sxs-lookup"><span data-stu-id="5eb15-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="5eb15-107">示例</span><span class="sxs-lookup"><span data-stu-id="5eb15-107">EXAMPLES</span></span>

### <span data-ttu-id="5eb15-108">範例1移除 IotHub</span><span class="sxs-lookup"><span data-stu-id="5eb15-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5eb15-109">移除名為 "myiothub" 的 IotHub</span><span class="sxs-lookup"><span data-stu-id="5eb15-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="5eb15-110">參數</span><span class="sxs-lookup"><span data-stu-id="5eb15-110">PARAMETERS</span></span>

### <span data-ttu-id="5eb15-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="5eb15-111">-Name</span></span>
<span data-ttu-id="5eb15-112">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="5eb15-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="5eb15-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb15-113">-ResourceGroupName</span></span>
<span data-ttu-id="5eb15-114">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5eb15-114">Resource Group Name</span></span>

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

### <span data-ttu-id="5eb15-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5eb15-115">-Confirm</span></span>
<span data-ttu-id="5eb15-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5eb15-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb15-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb15-117">-WhatIf</span></span>
<span data-ttu-id="5eb15-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5eb15-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb15-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5eb15-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb15-120">-DefaultProfile</span></span>
<span data-ttu-id="5eb15-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eb15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eb15-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb15-122">CommonParameters</span></span>
<span data-ttu-id="5eb15-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5eb15-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb15-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5eb15-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb15-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5eb15-125">INPUTS</span></span>

### <span data-ttu-id="5eb15-126">System.object</span><span class="sxs-lookup"><span data-stu-id="5eb15-126">System.String</span></span>

## <span data-ttu-id="5eb15-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5eb15-127">OUTPUTS</span></span>

### <span data-ttu-id="5eb15-128">System.object</span><span class="sxs-lookup"><span data-stu-id="5eb15-128">System.Object</span></span>

## <span data-ttu-id="5eb15-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5eb15-129">NOTES</span></span>

## <span data-ttu-id="5eb15-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eb15-130">RELATED LINKS</span></span>

