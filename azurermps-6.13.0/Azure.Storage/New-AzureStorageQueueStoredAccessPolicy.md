---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: ea317e4fba3a1c92b55a4cab1acb46873b1d5c92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450388"
---
# <span data-ttu-id="89465-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89465-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="89465-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89465-102">SYNOPSIS</span></span>
<span data-ttu-id="89465-103">建立 Azure 儲存空間佇列的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="89465-103">Creates a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89465-104">句法</span><span class="sxs-lookup"><span data-stu-id="89465-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89465-105">說明</span><span class="sxs-lookup"><span data-stu-id="89465-105">DESCRIPTION</span></span>
<span data-ttu-id="89465-106">**新的-AzureStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="89465-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="89465-107">示例</span><span class="sxs-lookup"><span data-stu-id="89465-107">EXAMPLES</span></span>

### <span data-ttu-id="89465-108">範例1：在儲存佇列中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="89465-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="89465-109">這個命令會在名為 MyQueue 的儲存佇列中建立名為 Policy01 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="89465-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="89465-110">參數</span><span class="sxs-lookup"><span data-stu-id="89465-110">PARAMETERS</span></span>

### <span data-ttu-id="89465-111">-內容</span><span class="sxs-lookup"><span data-stu-id="89465-111">-Context</span></span>
<span data-ttu-id="89465-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="89465-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="89465-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89465-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="89465-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89465-114">-DefaultProfile</span></span>
<span data-ttu-id="89465-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89465-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89465-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="89465-116">-ExpiryTime</span></span>
<span data-ttu-id="89465-117">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="89465-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="89465-118">-許可權</span><span class="sxs-lookup"><span data-stu-id="89465-118">-Permission</span></span>
<span data-ttu-id="89465-119">指定儲存的存取原則中的許可權，以存取儲存佇列。</span><span class="sxs-lookup"><span data-stu-id="89465-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="89465-120">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="89465-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="89465-121">-原則</span><span class="sxs-lookup"><span data-stu-id="89465-121">-Policy</span></span>
<span data-ttu-id="89465-122">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="89465-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="89465-123">-佇列</span><span class="sxs-lookup"><span data-stu-id="89465-123">-Queue</span></span>
<span data-ttu-id="89465-124">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="89465-124">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="89465-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="89465-125">-StartTime</span></span>
<span data-ttu-id="89465-126">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="89465-126">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="89465-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89465-127">CommonParameters</span></span>
<span data-ttu-id="89465-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89465-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89465-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89465-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89465-130">輸入</span><span class="sxs-lookup"><span data-stu-id="89465-130">INPUTS</span></span>

### <span data-ttu-id="89465-131">System.object</span><span class="sxs-lookup"><span data-stu-id="89465-131">System.String</span></span>

### <span data-ttu-id="89465-132">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="89465-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="89465-133">輸出</span><span class="sxs-lookup"><span data-stu-id="89465-133">OUTPUTS</span></span>

### <span data-ttu-id="89465-134">System.object</span><span class="sxs-lookup"><span data-stu-id="89465-134">System.String</span></span>

## <span data-ttu-id="89465-135">筆記</span><span class="sxs-lookup"><span data-stu-id="89465-135">NOTES</span></span>

## <span data-ttu-id="89465-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="89465-136">RELATED LINKS</span></span>

[<span data-ttu-id="89465-137">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89465-137">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="89465-138">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="89465-138">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="89465-139">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89465-139">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="89465-140">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89465-140">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)

