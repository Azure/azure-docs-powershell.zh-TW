---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904802"
---
# <span data-ttu-id="2eed9-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2eed9-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="2eed9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2eed9-102">SYNOPSIS</span></span>
<span data-ttu-id="2eed9-103">建立 Azure 儲存資料表的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="2eed9-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2eed9-104">語法</span><span class="sxs-lookup"><span data-stu-id="2eed9-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eed9-105">描述</span><span class="sxs-lookup"><span data-stu-id="2eed9-105">DESCRIPTION</span></span>
<span data-ttu-id="2eed9-106">**New-AzStorageTableStoredAccessPolicy** Cmdlet 會建立 Azure 儲存資料表的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="2eed9-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="2eed9-107">例子</span><span class="sxs-lookup"><span data-stu-id="2eed9-107">EXAMPLES</span></span>

### <span data-ttu-id="2eed9-108">範例 1：在資料表中建立儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="2eed9-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="2eed9-109">此命令在名為 MyTable 的儲存資料表中建立一個名為 Policy02 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="2eed9-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="2eed9-110">參數</span><span class="sxs-lookup"><span data-stu-id="2eed9-110">PARAMETERS</span></span>

### <span data-ttu-id="2eed9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2eed9-111">-Context</span></span>
<span data-ttu-id="2eed9-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2eed9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2eed9-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2eed9-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eed9-114">-DefaultProfile</span></span>
<span data-ttu-id="2eed9-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2eed9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2eed9-116">-ExpiryTime</span></span>
<span data-ttu-id="2eed9-117">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="2eed9-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-118">-許可權</span><span class="sxs-lookup"><span data-stu-id="2eed9-118">-Permission</span></span>
<span data-ttu-id="2eed9-119">指定儲存存取策略中存取儲存資料表的許可權。</span><span class="sxs-lookup"><span data-stu-id="2eed9-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="2eed9-120">請注意，這是一個字串，例如用於讀取 (新增、更新 `raud` 和刪除) 。</span><span class="sxs-lookup"><span data-stu-id="2eed9-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-121">-策略</span><span class="sxs-lookup"><span data-stu-id="2eed9-121">-Policy</span></span>
<span data-ttu-id="2eed9-122">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="2eed9-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2eed9-123">-StartTime</span></span>
<span data-ttu-id="2eed9-124">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="2eed9-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-125">-表格</span><span class="sxs-lookup"><span data-stu-id="2eed9-125">-Table</span></span>
<span data-ttu-id="2eed9-126">指定 Azure 儲存資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="2eed9-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eed9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eed9-127">CommonParameters</span></span>
<span data-ttu-id="2eed9-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2eed9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eed9-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2eed9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eed9-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2eed9-130">INPUTS</span></span>

### <span data-ttu-id="2eed9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2eed9-131">System.String</span></span>

### <span data-ttu-id="2eed9-132">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2eed9-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2eed9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2eed9-133">OUTPUTS</span></span>

### <span data-ttu-id="2eed9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2eed9-134">System.String</span></span>

## <span data-ttu-id="2eed9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2eed9-135">NOTES</span></span>

## <span data-ttu-id="2eed9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2eed9-136">RELATED LINKS</span></span>

[<span data-ttu-id="2eed9-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2eed9-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2eed9-138">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2eed9-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2eed9-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2eed9-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="2eed9-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2eed9-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


