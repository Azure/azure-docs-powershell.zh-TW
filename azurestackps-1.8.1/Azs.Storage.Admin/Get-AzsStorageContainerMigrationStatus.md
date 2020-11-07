---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793933"
---
# <span data-ttu-id="4e00b-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="4e00b-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="4e00b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e00b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e00b-103">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e00b-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="4e00b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e00b-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e00b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e00b-105">DESCRIPTION</span></span>
<span data-ttu-id="4e00b-106">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e00b-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="4e00b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e00b-107">EXAMPLES</span></span>

### <span data-ttu-id="4e00b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e00b-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="4e00b-109">取得容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e00b-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="4e00b-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e00b-110">PARAMETERS</span></span>

### <span data-ttu-id="4e00b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="4e00b-111">-FarmName</span></span>
<span data-ttu-id="4e00b-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="4e00b-112">Farm Id.</span></span>

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

### <span data-ttu-id="4e00b-113">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="4e00b-113">-JobId</span></span>
<span data-ttu-id="4e00b-114">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="4e00b-114">Operation Id.</span></span>

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

### <span data-ttu-id="4e00b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e00b-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e00b-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4e00b-116">Resource group name.</span></span>

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

### <span data-ttu-id="4e00b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e00b-117">CommonParameters</span></span>
<span data-ttu-id="4e00b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e00b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e00b-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e00b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e00b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4e00b-120">INPUTS</span></span>

## <span data-ttu-id="4e00b-121">輸出</span><span class="sxs-lookup"><span data-stu-id="4e00b-121">OUTPUTS</span></span>

### <span data-ttu-id="4e00b-122">AzureStack （MigrationResult）的</span><span class="sxs-lookup"><span data-stu-id="4e00b-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="4e00b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="4e00b-123">NOTES</span></span>

## <span data-ttu-id="4e00b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e00b-124">RELATED LINKS</span></span>
