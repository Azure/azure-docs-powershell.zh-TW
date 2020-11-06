---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0207d9d2353954fc1997f5752ac6dad26dbdfa13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442940"
---
# <span data-ttu-id="0ad04-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="0ad04-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="0ad04-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ad04-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad04-103">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="0ad04-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="0ad04-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ad04-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad04-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ad04-105">DESCRIPTION</span></span>
<span data-ttu-id="0ad04-106">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="0ad04-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="0ad04-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ad04-107">EXAMPLES</span></span>

### <span data-ttu-id="0ad04-108">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0ad04-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="0ad04-109">取得容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="0ad04-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="0ad04-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ad04-110">PARAMETERS</span></span>

### <span data-ttu-id="0ad04-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="0ad04-111">-FarmName</span></span>
<span data-ttu-id="0ad04-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="0ad04-112">Farm Id.</span></span>

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

### <span data-ttu-id="0ad04-113">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="0ad04-113">-JobId</span></span>
<span data-ttu-id="0ad04-114">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="0ad04-114">Operation Id.</span></span>

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

### <span data-ttu-id="0ad04-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad04-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ad04-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0ad04-116">Resource group name.</span></span>

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

### <span data-ttu-id="0ad04-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad04-117">CommonParameters</span></span>
<span data-ttu-id="0ad04-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ad04-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad04-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ad04-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad04-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0ad04-120">INPUTS</span></span>

## <span data-ttu-id="0ad04-121">輸出</span><span class="sxs-lookup"><span data-stu-id="0ad04-121">OUTPUTS</span></span>

### <span data-ttu-id="0ad04-122">AzureStack （MigrationResult）的</span><span class="sxs-lookup"><span data-stu-id="0ad04-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="0ad04-123">筆記</span><span class="sxs-lookup"><span data-stu-id="0ad04-123">NOTES</span></span>

## <span data-ttu-id="0ad04-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ad04-124">RELATED LINKS</span></span>

