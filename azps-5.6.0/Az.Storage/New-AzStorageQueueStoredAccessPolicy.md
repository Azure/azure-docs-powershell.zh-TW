---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f676f644cb69880a0b403a4e656ce9cb435b7c77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915050"
---
# <span data-ttu-id="f5532-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5532-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="f5532-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5532-102">SYNOPSIS</span></span>
<span data-ttu-id="f5532-103">建立 Azure 儲存佇列的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="f5532-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f5532-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5532-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5532-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5532-105">DESCRIPTION</span></span>
<span data-ttu-id="f5532-106">**New-AzStorageQueueStoredAccessPolicy** Cmdlet 會建立 Azure 儲存佇列的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="f5532-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="f5532-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5532-107">EXAMPLES</span></span>

### <span data-ttu-id="f5532-108">範例 1：在儲存佇列中建立儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="f5532-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="f5532-109">此命令在名為 MyQueue 的儲存佇列中建立一個名為 Policy01 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="f5532-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="f5532-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5532-110">PARAMETERS</span></span>

### <span data-ttu-id="f5532-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f5532-111">-Context</span></span>
<span data-ttu-id="f5532-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="f5532-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f5532-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5532-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f5532-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5532-114">-DefaultProfile</span></span>
<span data-ttu-id="f5532-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5532-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5532-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f5532-116">-ExpiryTime</span></span>
<span data-ttu-id="f5532-117">指定儲存的存取策略變成不正確時間。</span><span class="sxs-lookup"><span data-stu-id="f5532-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="f5532-118">-許可權</span><span class="sxs-lookup"><span data-stu-id="f5532-118">-Permission</span></span>
<span data-ttu-id="f5532-119">指定儲存存取策略中存取儲存佇列的許可權。</span><span class="sxs-lookup"><span data-stu-id="f5532-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="f5532-120">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="f5532-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="f5532-121">-策略</span><span class="sxs-lookup"><span data-stu-id="f5532-121">-Policy</span></span>
<span data-ttu-id="f5532-122">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5532-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="f5532-123">-佇列</span><span class="sxs-lookup"><span data-stu-id="f5532-123">-Queue</span></span>
<span data-ttu-id="f5532-124">指定 Azure 儲存佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="f5532-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="f5532-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f5532-125">-StartTime</span></span>
<span data-ttu-id="f5532-126">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="f5532-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="f5532-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5532-127">CommonParameters</span></span>
<span data-ttu-id="f5532-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5532-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5532-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f5532-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5532-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f5532-130">INPUTS</span></span>

### <span data-ttu-id="f5532-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f5532-131">System.String</span></span>

### <span data-ttu-id="f5532-132">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5532-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f5532-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f5532-133">OUTPUTS</span></span>

### <span data-ttu-id="f5532-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f5532-134">System.String</span></span>

## <span data-ttu-id="f5532-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f5532-135">NOTES</span></span>

## <span data-ttu-id="f5532-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5532-136">RELATED LINKS</span></span>

[<span data-ttu-id="f5532-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5532-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f5532-138">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5532-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f5532-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5532-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f5532-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f5532-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


