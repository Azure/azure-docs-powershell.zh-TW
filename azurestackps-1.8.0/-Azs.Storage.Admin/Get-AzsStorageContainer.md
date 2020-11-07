---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793717"
---
# <span data-ttu-id="f34ff-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f34ff-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="f34ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f34ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f34ff-103">傳回可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="f34ff-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f34ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="f34ff-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f34ff-105">說明</span><span class="sxs-lookup"><span data-stu-id="f34ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f34ff-106">傳回可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="f34ff-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f34ff-107">示例</span><span class="sxs-lookup"><span data-stu-id="f34ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f34ff-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f34ff-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="f34ff-109">取得可在指定的共用中遷移的容器清單。</span><span class="sxs-lookup"><span data-stu-id="f34ff-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="f34ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="f34ff-110">PARAMETERS</span></span>

### <span data-ttu-id="f34ff-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="f34ff-111">-FarmName</span></span>
<span data-ttu-id="f34ff-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="f34ff-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ff-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f34ff-113">-MaxCount</span></span>
<span data-ttu-id="f34ff-114">容器的最大數目。</span><span class="sxs-lookup"><span data-stu-id="f34ff-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f34ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="f34ff-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f34ff-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ff-117">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="f34ff-117">-ShareName</span></span>
<span data-ttu-id="f34ff-118">存放儲存容器的共用名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f34ff-118">Share name which holds the storage containers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ff-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="f34ff-119">-StartIndex</span></span>
<span data-ttu-id="f34ff-120">[取得容器] 的起始索引。</span><span class="sxs-lookup"><span data-stu-id="f34ff-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f34ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f34ff-121">CommonParameters</span></span>
<span data-ttu-id="f34ff-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f34ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f34ff-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f34ff-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f34ff-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f34ff-124">INPUTS</span></span>

## <span data-ttu-id="f34ff-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f34ff-125">OUTPUTS</span></span>

## <span data-ttu-id="f34ff-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f34ff-126">NOTES</span></span>

## <span data-ttu-id="f34ff-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f34ff-127">RELATED LINKS</span></span>

