---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 578eef176903576778325eb8610870040a515751
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623212"
---
# <span data-ttu-id="61733-101">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61733-101">New-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="61733-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61733-102">SYNOPSIS</span></span>
<span data-ttu-id="61733-103">建立 Azure 儲存空間佇列的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="61733-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="61733-104">句法</span><span class="sxs-lookup"><span data-stu-id="61733-104">SYNTAX</span></span>

```
New-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="61733-105">說明</span><span class="sxs-lookup"><span data-stu-id="61733-105">DESCRIPTION</span></span>
<span data-ttu-id="61733-106">**新的-AzureStorageQueueStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間佇列建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="61733-106">The **New-AzureStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="61733-107">示例</span><span class="sxs-lookup"><span data-stu-id="61733-107">EXAMPLES</span></span>

### <span data-ttu-id="61733-108">範例1：在儲存佇列中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="61733-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="61733-109">這個命令會在名為 MyQueue 的儲存佇列中建立名為 Policy01 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="61733-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="61733-110">參數</span><span class="sxs-lookup"><span data-stu-id="61733-110">PARAMETERS</span></span>

### <span data-ttu-id="61733-111">-內容</span><span class="sxs-lookup"><span data-stu-id="61733-111">-Context</span></span>
<span data-ttu-id="61733-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="61733-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="61733-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61733-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61733-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="61733-114">-ExpiryTime</span></span>
<span data-ttu-id="61733-115">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="61733-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61733-116">-許可權</span><span class="sxs-lookup"><span data-stu-id="61733-116">-Permission</span></span>
<span data-ttu-id="61733-117">指定此儲存佇列的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="61733-117">Specifies the level of public access to this storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61733-118">-原則</span><span class="sxs-lookup"><span data-stu-id="61733-118">-Policy</span></span>
<span data-ttu-id="61733-119">指定儲存的存取原則，包括此 SAS 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="61733-119">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="61733-120">-佇列</span><span class="sxs-lookup"><span data-stu-id="61733-120">-Queue</span></span>
<span data-ttu-id="61733-121">指定 Azure 儲存空間佇列名稱。</span><span class="sxs-lookup"><span data-stu-id="61733-121">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61733-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="61733-122">-StartTime</span></span>
<span data-ttu-id="61733-123">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="61733-123">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61733-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61733-124">CommonParameters</span></span>
<span data-ttu-id="61733-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61733-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61733-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61733-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61733-127">輸入</span><span class="sxs-lookup"><span data-stu-id="61733-127">INPUTS</span></span>

## <span data-ttu-id="61733-128">輸出</span><span class="sxs-lookup"><span data-stu-id="61733-128">OUTPUTS</span></span>

## <span data-ttu-id="61733-129">筆記</span><span class="sxs-lookup"><span data-stu-id="61733-129">NOTES</span></span>

## <span data-ttu-id="61733-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="61733-130">RELATED LINKS</span></span>

[<span data-ttu-id="61733-131">AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61733-131">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="61733-132">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="61733-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="61733-133">移除-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61733-133">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="61733-134">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="61733-134">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)


