---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: eff689d36268f7eaec045c05c00d4fd18e91a026
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2020
ms.locfileid: "93793820"
---
# <span data-ttu-id="cd3a4-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="cd3a4-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="cd3a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd3a4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3a4-103">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-103">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="cd3a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd3a4-104">SYNTAX</span></span>

### <span data-ttu-id="cd3a4-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="cd3a4-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="cd3a4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="cd3a4-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="cd3a4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd3a4-107">ResourceId</span></span>
```
Get-AzsDirectoryTenant -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="cd3a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="cd3a4-108">DESCRIPTION</span></span>
<span data-ttu-id="cd3a4-109">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-109">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="cd3a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="cd3a4-110">EXAMPLES</span></span>

### <span data-ttu-id="cd3a4-111">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cd3a4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName "System.Local"
```

<span data-ttu-id="cd3a4-112">列出目前訂閱與指定資源群組名稱下的所有目錄租使用者。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="cd3a4-113">參數</span><span class="sxs-lookup"><span data-stu-id="cd3a4-113">PARAMETERS</span></span>

### <span data-ttu-id="cd3a4-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd3a4-114">-Name</span></span>
<span data-ttu-id="cd3a4-115">目錄租使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-115">Directory tenant name.</span></span>

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

### <span data-ttu-id="cd3a4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3a4-116">-ResourceGroupName</span></span>
<span data-ttu-id="cd3a4-117">{{Fill ResourceGroupName 說明}}</span><span class="sxs-lookup"><span data-stu-id="cd3a4-117">{{Fill ResourceGroupName Description}}</span></span>

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

### <span data-ttu-id="cd3a4-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd3a4-118">-ResourceId</span></span>
<span data-ttu-id="cd3a4-119">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-119">The resource id.</span></span>

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

### <span data-ttu-id="cd3a4-120">-略過</span><span class="sxs-lookup"><span data-stu-id="cd3a4-120">-Skip</span></span>
<span data-ttu-id="cd3a4-121">略過參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="cd3a4-122">-上方</span><span class="sxs-lookup"><span data-stu-id="cd3a4-122">-Top</span></span>
<span data-ttu-id="cd3a4-123">傳回參數值所指定的前 N 個專案。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="cd3a4-124">在-Skip 參數後套用。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="cd3a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3a4-125">CommonParameters</span></span>
<span data-ttu-id="cd3a4-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3a4-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3a4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="cd3a4-128">INPUTS</span></span>

## <span data-ttu-id="cd3a4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cd3a4-129">OUTPUTS</span></span>

### <span data-ttu-id="cd3a4-130">AzureStack DirectoryTenant 的訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd3a4-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DirectoryTenant</span></span>

## <span data-ttu-id="cd3a4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cd3a4-131">NOTES</span></span>

## <span data-ttu-id="cd3a4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd3a4-132">RELATED LINKS</span></span>

