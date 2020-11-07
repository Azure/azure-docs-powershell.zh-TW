---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4ec0639e31df3766550d6f7acc655cd3b5608bf
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793944"
---
# <span data-ttu-id="8d2c5-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8d2c5-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="8d2c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2c5-103">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="8d2c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d2c5-104">SYNTAX</span></span>

### <span data-ttu-id="8d2c5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8d2c5-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8d2c5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8d2c5-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d2c5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d2c5-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="8d2c5-108">說明</span><span class="sxs-lookup"><span data-stu-id="8d2c5-108">DESCRIPTION</span></span>
<span data-ttu-id="8d2c5-109">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="8d2c5-110">示例</span><span class="sxs-lookup"><span data-stu-id="8d2c5-110">EXAMPLES</span></span>

### <span data-ttu-id="8d2c5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8d2c5-111">EXAMPLE 1</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="8d2c5-112">取得儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="8d2c5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8d2c5-113">EXAMPLE 2</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="8d2c5-114">取得指定儲存空間帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="8d2c5-115">參數</span><span class="sxs-lookup"><span data-stu-id="8d2c5-115">PARAMETERS</span></span>

### <span data-ttu-id="8d2c5-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8d2c5-116">-FarmName</span></span>
<span data-ttu-id="8d2c5-117">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-117">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d2c5-118">-Name</span></span>
<span data-ttu-id="8d2c5-119">租使用者看不到的內部儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="8d2c5-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-121">Resource group name.</span></span>

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

### <span data-ttu-id="8d2c5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d2c5-122">-ResourceId</span></span>
<span data-ttu-id="8d2c5-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-124">-摘要</span><span class="sxs-lookup"><span data-stu-id="8d2c5-124">-Summary</span></span>
<span data-ttu-id="8d2c5-125">已傳回 wheter 摘要或詳細資訊的切換。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-125">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-126">-略過</span><span class="sxs-lookup"><span data-stu-id="8d2c5-126">-Skip</span></span>
<span data-ttu-id="8d2c5-127">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-127">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-128">-上方</span><span class="sxs-lookup"><span data-stu-id="8d2c5-128">-Top</span></span>
<span data-ttu-id="8d2c5-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8d2c5-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2c5-131">CommonParameters</span></span>
<span data-ttu-id="8d2c5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2c5-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d2c5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2c5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8d2c5-134">INPUTS</span></span>

## <span data-ttu-id="8d2c5-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8d2c5-135">OUTPUTS</span></span>

### <span data-ttu-id="8d2c5-136">AzureStack （StorageAccount）的</span><span class="sxs-lookup"><span data-stu-id="8d2c5-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="8d2c5-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8d2c5-137">NOTES</span></span>

## <span data-ttu-id="8d2c5-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d2c5-138">RELATED LINKS</span></span>
