---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793852"
---
# <span data-ttu-id="f6195-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="f6195-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="f6195-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6195-102">SYNOPSIS</span></span>
<span data-ttu-id="f6195-103">傳回特定位置上所有結構檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="f6195-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="f6195-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6195-104">SYNTAX</span></span>

### <span data-ttu-id="f6195-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f6195-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6195-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f6195-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6195-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6195-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f6195-108">說明</span><span class="sxs-lookup"><span data-stu-id="f6195-108">DESCRIPTION</span></span>
<span data-ttu-id="f6195-109">傳回特定位置上所有結構檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="f6195-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="f6195-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6195-110">EXAMPLES</span></span>

### <span data-ttu-id="f6195-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f6195-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="f6195-112">傳回所有檔案共用的清單。</span><span class="sxs-lookup"><span data-stu-id="f6195-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="f6195-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f6195-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="f6195-114">根據名稱返回檔案共用。</span><span class="sxs-lookup"><span data-stu-id="f6195-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="f6195-115">參數</span><span class="sxs-lookup"><span data-stu-id="f6195-115">PARAMETERS</span></span>

### <span data-ttu-id="f6195-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6195-116">-Name</span></span>
<span data-ttu-id="f6195-117">Fabric 檔案共用名稱。</span><span class="sxs-lookup"><span data-stu-id="f6195-117">Fabric file share name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6195-118">-位置</span><span class="sxs-lookup"><span data-stu-id="f6195-118">-Location</span></span>
<span data-ttu-id="f6195-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="f6195-119">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6195-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6195-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6195-121">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f6195-121">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6195-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6195-122">-ResourceId</span></span>
<span data-ttu-id="f6195-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f6195-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6195-124">-篩選</span><span class="sxs-lookup"><span data-stu-id="f6195-124">-Filter</span></span>
<span data-ttu-id="f6195-125">OData 篩選參數。</span><span class="sxs-lookup"><span data-stu-id="f6195-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6195-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6195-126">CommonParameters</span></span>
<span data-ttu-id="f6195-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6195-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6195-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6195-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6195-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f6195-129">INPUTS</span></span>

## <span data-ttu-id="f6195-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f6195-130">OUTPUTS</span></span>

### <span data-ttu-id="f6195-131">AzureStack. 系統管理.............。</span><span class="sxs-lookup"><span data-stu-id="f6195-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="f6195-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f6195-132">NOTES</span></span>

## <span data-ttu-id="f6195-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6195-133">RELATED LINKS</span></span>
