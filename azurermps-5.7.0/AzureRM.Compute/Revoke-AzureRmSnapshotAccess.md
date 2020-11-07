---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625914"
---
# <span data-ttu-id="95c14-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="95c14-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="95c14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95c14-102">SYNOPSIS</span></span>
<span data-ttu-id="95c14-103">吊銷快照存取權。</span><span class="sxs-lookup"><span data-stu-id="95c14-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95c14-104">句法</span><span class="sxs-lookup"><span data-stu-id="95c14-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="95c14-105">說明</span><span class="sxs-lookup"><span data-stu-id="95c14-105">DESCRIPTION</span></span>
<span data-ttu-id="95c14-106">**Revoke AzureRmSnapshotAccess** Cmdlet 會吊銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="95c14-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="95c14-107">示例</span><span class="sxs-lookup"><span data-stu-id="95c14-107">EXAMPLES</span></span>

### <span data-ttu-id="95c14-108">範例1</span><span class="sxs-lookup"><span data-stu-id="95c14-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="95c14-109">廢除名為「ResourceGroup01」的資源群組中名為「Snapshot01」的快照存取權</span><span class="sxs-lookup"><span data-stu-id="95c14-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="95c14-110">參數</span><span class="sxs-lookup"><span data-stu-id="95c14-110">PARAMETERS</span></span>

### <span data-ttu-id="95c14-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95c14-111">-ResourceGroupName</span></span>
<span data-ttu-id="95c14-112">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95c14-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="95c14-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="95c14-113">-SnapshotName</span></span>
<span data-ttu-id="95c14-114">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="95c14-114">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95c14-115">-確認</span><span class="sxs-lookup"><span data-stu-id="95c14-115">-Confirm</span></span>
<span data-ttu-id="95c14-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="95c14-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c14-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95c14-117">-WhatIf</span></span>
<span data-ttu-id="95c14-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="95c14-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95c14-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95c14-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95c14-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95c14-120">CommonParameters</span></span>
<span data-ttu-id="95c14-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95c14-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95c14-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95c14-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95c14-123">輸入</span><span class="sxs-lookup"><span data-stu-id="95c14-123">INPUTS</span></span>

### <span data-ttu-id="95c14-124">System.object</span><span class="sxs-lookup"><span data-stu-id="95c14-124">System.String</span></span>

## <span data-ttu-id="95c14-125">輸出</span><span class="sxs-lookup"><span data-stu-id="95c14-125">OUTPUTS</span></span>

### <span data-ttu-id="95c14-126">System.object</span><span class="sxs-lookup"><span data-stu-id="95c14-126">System.Object</span></span>

## <span data-ttu-id="95c14-127">筆記</span><span class="sxs-lookup"><span data-stu-id="95c14-127">NOTES</span></span>

## <span data-ttu-id="95c14-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="95c14-128">RELATED LINKS</span></span>

