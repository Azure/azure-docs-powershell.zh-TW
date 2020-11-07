---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 96220d7bac0a71f579f81a4d01f4f1dc3cba9dd1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968337"
---
# <span data-ttu-id="eb6a3-101">Get-AzsStorageContainerMigrationStatus</span><span class="sxs-lookup"><span data-stu-id="eb6a3-101">Get-AzsStorageContainerMigrationStatus</span></span>

## <span data-ttu-id="eb6a3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6a3-103">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-103">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="eb6a3-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb6a3-104">SYNTAX</span></span>

```
Get-AzsStorageContainerMigrationStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6a3-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb6a3-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6a3-106">傳回容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-106">Returns the status of a container migration job.</span></span>

## <span data-ttu-id="eb6a3-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb6a3-107">EXAMPLES</span></span>

### <span data-ttu-id="eb6a3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="eb6a3-108">EXAMPLE 1</span></span>
```
Get-AzsStorageContainerMigrationStatus -FarmName "6ed442a3-ec47-4145-b2f0-9b90377b01d0" -JobId "6478ef3b-b7d5-4827-8d47-551c6afb9dd4"
```

<span data-ttu-id="eb6a3-109">取得容器遷移工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-109">Get the status of a container migration job.</span></span>

## <span data-ttu-id="eb6a3-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb6a3-110">PARAMETERS</span></span>

### <span data-ttu-id="eb6a3-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="eb6a3-111">-FarmName</span></span>
<span data-ttu-id="eb6a3-112">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-112">Farm Id.</span></span>

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

### <span data-ttu-id="eb6a3-113">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="eb6a3-113">-JobId</span></span>
<span data-ttu-id="eb6a3-114">操作 Id。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-114">Operation Id.</span></span>

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

### <span data-ttu-id="eb6a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb6a3-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-116">Resource group name.</span></span>

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

### <span data-ttu-id="eb6a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6a3-117">CommonParameters</span></span>
<span data-ttu-id="eb6a3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6a3-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb6a3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6a3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="eb6a3-120">INPUTS</span></span>

## <span data-ttu-id="eb6a3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="eb6a3-121">OUTPUTS</span></span>

### <span data-ttu-id="eb6a3-122">AzureStack （MigrationResult）的</span><span class="sxs-lookup"><span data-stu-id="eb6a3-122">Microsoft.AzureStack.Management.Storage.Admin.Models.MigrationResult</span></span>

## <span data-ttu-id="eb6a3-123">筆記</span><span class="sxs-lookup"><span data-stu-id="eb6a3-123">NOTES</span></span>

## <span data-ttu-id="eb6a3-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb6a3-124">RELATED LINKS</span></span>
