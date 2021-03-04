---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F1EC601C-3ADD-402A-A5F7-84A95D312187
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: fbd5adc202886ae987f7739ac24d1dadbc0d41d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909281"
---
# <span data-ttu-id="920c7-101">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="920c7-101">Get-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="920c7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="920c7-102">SYNOPSIS</span></span>
<span data-ttu-id="920c7-103">取得 Azure 儲存佇列的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="920c7-103">Gets the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="920c7-104">語法</span><span class="sxs-lookup"><span data-stu-id="920c7-104">SYNTAX</span></span>

```
Get-AzStorageQueueStoredAccessPolicy [-Queue] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="920c7-105">描述</span><span class="sxs-lookup"><span data-stu-id="920c7-105">DESCRIPTION</span></span>
<span data-ttu-id="920c7-106">**Get-AzStorageQueueStoredAccessPolicy** Cmdlet 會列出 Azure 儲存佇列的儲存存取策略或策略。</span><span class="sxs-lookup"><span data-stu-id="920c7-106">The **Get-AzStorageQueueStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage queue.</span></span>

## <span data-ttu-id="920c7-107">例子</span><span class="sxs-lookup"><span data-stu-id="920c7-107">EXAMPLES</span></span>

### <span data-ttu-id="920c7-108">範例 1：在佇列中取得儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="920c7-108">Example 1: Get a stored access policy in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy12"
```

<span data-ttu-id="920c7-109">此命令會取得名為 MyQueue 的儲存佇列中名為 Policy12 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="920c7-109">This command gets the access policy named Policy12 in the storage queue named MyQueue.</span></span>

### <span data-ttu-id="920c7-110">範例 2：在佇列中取得所有儲存的存取策略</span><span class="sxs-lookup"><span data-stu-id="920c7-110">Example 2: Get all stored access policies in the queue</span></span>
```
PS C:\>Get-AzStorageQueueStoredAccessPolicy -Queue "MyQueue"
```

<span data-ttu-id="920c7-111">此命令會取得佇列中名為 MyQueue 的所有儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="920c7-111">This command gets all stored access policies in the queue named MyQueue.</span></span>

## <span data-ttu-id="920c7-112">參數</span><span class="sxs-lookup"><span data-stu-id="920c7-112">PARAMETERS</span></span>

### <span data-ttu-id="920c7-113">-內容</span><span class="sxs-lookup"><span data-stu-id="920c7-113">-Context</span></span>
<span data-ttu-id="920c7-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="920c7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="920c7-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="920c7-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="920c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920c7-116">-DefaultProfile</span></span>
<span data-ttu-id="920c7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="920c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="920c7-118">-策略</span><span class="sxs-lookup"><span data-stu-id="920c7-118">-Policy</span></span>
<span data-ttu-id="920c7-119">指定儲存的存取策略，包括此共用存取簽章的許可權 (SAS) 權杖。</span><span class="sxs-lookup"><span data-stu-id="920c7-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="920c7-120">-佇列</span><span class="sxs-lookup"><span data-stu-id="920c7-120">-Queue</span></span>
<span data-ttu-id="920c7-121">指定 Azure 儲存佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="920c7-121">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="920c7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920c7-122">CommonParameters</span></span>
<span data-ttu-id="920c7-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="920c7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920c7-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="920c7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920c7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="920c7-125">INPUTS</span></span>

### <span data-ttu-id="920c7-126">System.String</span><span class="sxs-lookup"><span data-stu-id="920c7-126">System.String</span></span>

### <span data-ttu-id="920c7-127">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="920c7-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="920c7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="920c7-128">OUTPUTS</span></span>

### <span data-ttu-id="920c7-129">Microsoft.Azure.storage.Queue.SharedAccessQueuePolicy</span><span class="sxs-lookup"><span data-stu-id="920c7-129">Microsoft.Azure.Storage.Queue.SharedAccessQueuePolicy</span></span>

## <span data-ttu-id="920c7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="920c7-130">NOTES</span></span>

## <span data-ttu-id="920c7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="920c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="920c7-132">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="920c7-132">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="920c7-133">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="920c7-133">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="920c7-134">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="920c7-134">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="920c7-135">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="920c7-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


