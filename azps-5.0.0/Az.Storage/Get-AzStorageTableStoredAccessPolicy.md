---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: b17a294392ca4336d4a96e5d136ad4e321eb45a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137958"
---
# <span data-ttu-id="dd568-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd568-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="dd568-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd568-102">SYNOPSIS</span></span>
<span data-ttu-id="dd568-103">取得 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="dd568-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="dd568-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd568-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd568-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd568-105">DESCRIPTION</span></span>
<span data-ttu-id="dd568-106">**AzStorageTableStoredAccessPolicy** Cmdlet 會列出 Azure 儲存空間資料表的儲存存取原則或原則。</span><span class="sxs-lookup"><span data-stu-id="dd568-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="dd568-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd568-107">EXAMPLES</span></span>

### <span data-ttu-id="dd568-108">範例1：在儲存空間資料表中取得儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="dd568-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="dd568-109">這個命令會在名為 Table02 的儲存空間資料表中取得名為 Policy50 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="dd568-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="dd568-110">範例2：取得儲存空間資料表中所有已儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="dd568-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="dd568-111">這個命令會取得名為 Table02 的資料表中的所有存取原則。</span><span class="sxs-lookup"><span data-stu-id="dd568-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="dd568-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd568-112">PARAMETERS</span></span>

### <span data-ttu-id="dd568-113">-內容</span><span class="sxs-lookup"><span data-stu-id="dd568-113">-Context</span></span>
<span data-ttu-id="dd568-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="dd568-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="dd568-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd568-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="dd568-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd568-116">-DefaultProfile</span></span>
<span data-ttu-id="dd568-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd568-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd568-118">-原則</span><span class="sxs-lookup"><span data-stu-id="dd568-118">-Policy</span></span>
<span data-ttu-id="dd568-119">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="dd568-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="dd568-120">-資料表</span><span class="sxs-lookup"><span data-stu-id="dd568-120">-Table</span></span>
<span data-ttu-id="dd568-121">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="dd568-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="dd568-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd568-122">CommonParameters</span></span>
<span data-ttu-id="dd568-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd568-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd568-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd568-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd568-125">輸入</span><span class="sxs-lookup"><span data-stu-id="dd568-125">INPUTS</span></span>

### <span data-ttu-id="dd568-126">System.object</span><span class="sxs-lookup"><span data-stu-id="dd568-126">System.String</span></span>

### <span data-ttu-id="dd568-127">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="dd568-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd568-128">輸出</span><span class="sxs-lookup"><span data-stu-id="dd568-128">OUTPUTS</span></span>

### <span data-ttu-id="dd568-129">[WindowsAzure] SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="dd568-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="dd568-130">筆記</span><span class="sxs-lookup"><span data-stu-id="dd568-130">NOTES</span></span>

## <span data-ttu-id="dd568-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd568-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd568-132">新-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd568-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd568-133">移除-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd568-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd568-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="dd568-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="dd568-135">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="dd568-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


