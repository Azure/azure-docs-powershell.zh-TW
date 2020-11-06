---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442999"
---
# <span data-ttu-id="9051c-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9051c-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="9051c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9051c-102">SYNOPSIS</span></span>
<span data-ttu-id="9051c-103">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9051c-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="9051c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9051c-104">SYNTAX</span></span>

### <span data-ttu-id="9051c-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9051c-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9051c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9051c-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9051c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9051c-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="9051c-108">說明</span><span class="sxs-lookup"><span data-stu-id="9051c-108">DESCRIPTION</span></span>
<span data-ttu-id="9051c-109">傳回要求的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="9051c-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="9051c-110">示例</span><span class="sxs-lookup"><span data-stu-id="9051c-110">EXAMPLES</span></span>

### <span data-ttu-id="9051c-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9051c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="9051c-112">取得儲存空間帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="9051c-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="9051c-113">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9051c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="9051c-114">取得指定儲存空間帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9051c-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="9051c-115">參數</span><span class="sxs-lookup"><span data-stu-id="9051c-115">PARAMETERS</span></span>

### <span data-ttu-id="9051c-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9051c-116">-FarmName</span></span>
<span data-ttu-id="9051c-117">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="9051c-117">Farm Id.</span></span>

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

### <span data-ttu-id="9051c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9051c-118">-Name</span></span>
<span data-ttu-id="9051c-119">租使用者看不到的內部儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="9051c-119">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="9051c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9051c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9051c-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9051c-121">Resource group name.</span></span>

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

### <span data-ttu-id="9051c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9051c-122">-ResourceId</span></span>
<span data-ttu-id="9051c-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9051c-123">The resource id.</span></span>

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

### <span data-ttu-id="9051c-124">-略過</span><span class="sxs-lookup"><span data-stu-id="9051c-124">-Skip</span></span>
<span data-ttu-id="9051c-125">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="9051c-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9051c-126">-摘要</span><span class="sxs-lookup"><span data-stu-id="9051c-126">-Summary</span></span>
<span data-ttu-id="9051c-127">已傳回 wheter 摘要或詳細資訊的切換。</span><span class="sxs-lookup"><span data-stu-id="9051c-127">Switch for wheter summary or detailed information is returned.</span></span>

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

### <span data-ttu-id="9051c-128">-上方</span><span class="sxs-lookup"><span data-stu-id="9051c-128">-Top</span></span>
<span data-ttu-id="9051c-129">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="9051c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9051c-130">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="9051c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9051c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9051c-131">CommonParameters</span></span>
<span data-ttu-id="9051c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9051c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9051c-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9051c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9051c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9051c-134">INPUTS</span></span>

## <span data-ttu-id="9051c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9051c-135">OUTPUTS</span></span>

### <span data-ttu-id="9051c-136">AzureStack （StorageAccount）的</span><span class="sxs-lookup"><span data-stu-id="9051c-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="9051c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9051c-137">NOTES</span></span>

## <span data-ttu-id="9051c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="9051c-138">RELATED LINKS</span></span>

