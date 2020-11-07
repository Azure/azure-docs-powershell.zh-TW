---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968334"
---
# <span data-ttu-id="4a5f8-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="4a5f8-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="4a5f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5f8-103">傳回系統認為最適合遷移的目標共用清單。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="4a5f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a5f8-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a5f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="4a5f8-106">傳回系統認為最適合遷移的目標共用清單。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="4a5f8-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a5f8-107">EXAMPLES</span></span>

### <span data-ttu-id="4a5f8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4a5f8-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="4a5f8-109">取得系統認為最適合遷移的目的共用清單。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="4a5f8-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a5f8-110">PARAMETERS</span></span>

### <span data-ttu-id="4a5f8-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="4a5f8-111">-SourceShareName</span></span>
<span data-ttu-id="4a5f8-112">包含要遷移之容器之共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="4a5f8-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="4a5f8-113">-FarmName</span></span>
<span data-ttu-id="4a5f8-114">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-114">Farm Id.</span></span>

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

### <span data-ttu-id="4a5f8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5f8-115">-ResourceGroupName</span></span>
<span data-ttu-id="4a5f8-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-116">Resource group name.</span></span>

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

### <span data-ttu-id="4a5f8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5f8-117">CommonParameters</span></span>
<span data-ttu-id="4a5f8-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5f8-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a5f8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5f8-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4a5f8-120">INPUTS</span></span>

## <span data-ttu-id="4a5f8-121">輸出</span><span class="sxs-lookup"><span data-stu-id="4a5f8-121">OUTPUTS</span></span>

## <span data-ttu-id="4a5f8-122">筆記</span><span class="sxs-lookup"><span data-stu-id="4a5f8-122">NOTES</span></span>

## <span data-ttu-id="4a5f8-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a5f8-123">RELATED LINKS</span></span>
