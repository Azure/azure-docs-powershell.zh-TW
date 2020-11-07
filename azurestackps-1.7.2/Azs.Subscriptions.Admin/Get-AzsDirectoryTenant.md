---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ae30d06970d9533c32c96f33a1917fa8d2a6e41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793306"
---
# <span data-ttu-id="be568-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="be568-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="be568-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be568-102">SYNOPSIS</span></span>
<span data-ttu-id="be568-103">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="be568-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="be568-104">句法</span><span class="sxs-lookup"><span data-stu-id="be568-104">SYNTAX</span></span>

### <span data-ttu-id="be568-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="be568-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="be568-106">獲取</span><span class="sxs-lookup"><span data-stu-id="be568-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="be568-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="be568-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="be568-108">說明</span><span class="sxs-lookup"><span data-stu-id="be568-108">DESCRIPTION</span></span>
<span data-ttu-id="be568-109">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="be568-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="be568-110">示例</span><span class="sxs-lookup"><span data-stu-id="be568-110">EXAMPLES</span></span>

### <span data-ttu-id="be568-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="be568-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="be568-112">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="be568-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="be568-113">參數</span><span class="sxs-lookup"><span data-stu-id="be568-113">PARAMETERS</span></span>

### <span data-ttu-id="be568-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="be568-114">-Name</span></span>
<span data-ttu-id="be568-115">目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="be568-115">Directory tenant name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be568-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be568-116">-ResourceGroupName</span></span>
<span data-ttu-id="be568-117">資源所在的資源群組。</span><span class="sxs-lookup"><span data-stu-id="be568-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="be568-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be568-118">-ResourceId</span></span>
<span data-ttu-id="be568-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="be568-119">The resource id.</span></span>

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

### <span data-ttu-id="be568-120">-略過</span><span class="sxs-lookup"><span data-stu-id="be568-120">-Skip</span></span>
<span data-ttu-id="be568-121">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="be568-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="be568-122">-上方</span><span class="sxs-lookup"><span data-stu-id="be568-122">-Top</span></span>
<span data-ttu-id="be568-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="be568-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="be568-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="be568-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="be568-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be568-125">CommonParameters</span></span>
<span data-ttu-id="be568-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be568-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be568-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be568-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be568-128">輸入</span><span class="sxs-lookup"><span data-stu-id="be568-128">INPUTS</span></span>

## <span data-ttu-id="be568-129">輸出</span><span class="sxs-lookup"><span data-stu-id="be568-129">OUTPUTS</span></span>

### <span data-ttu-id="be568-130">AzureStack DirectoryTenant 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="be568-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="be568-131">筆記</span><span class="sxs-lookup"><span data-stu-id="be568-131">NOTES</span></span>

## <span data-ttu-id="be568-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="be568-132">RELATED LINKS</span></span>

