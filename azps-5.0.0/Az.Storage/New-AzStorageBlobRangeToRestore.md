---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138621"
---
# <span data-ttu-id="f75e5-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="f75e5-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="f75e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f75e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f75e5-103">建立 [Blob 範圍] 物件來還原儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f75e5-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="f75e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f75e5-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f75e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f75e5-105">DESCRIPTION</span></span>
<span data-ttu-id="f75e5-106">**AzStorageBlobRangeToRestore** Cmdlet 會建立可在 Restore-AzStorageBlobRange 中使用的 Blob 範圍物件。</span><span class="sxs-lookup"><span data-stu-id="f75e5-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="f75e5-107">示例</span><span class="sxs-lookup"><span data-stu-id="f75e5-107">EXAMPLES</span></span>

### <span data-ttu-id="f75e5-108">範例1：建立要還原的 blob 範圍</span><span class="sxs-lookup"><span data-stu-id="f75e5-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="f75e5-109">這個命令會建立一個要還原的 blob 範圍，這會從 container1/blob1 (包含) ，而結束于 container2/blob2 (排除) ]。</span><span class="sxs-lookup"><span data-stu-id="f75e5-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="f75e5-110">範例2：建立一個 blob 範圍，該範圍會從第一個 blob 依字母順序還原至特定的 blob (排除) </span><span class="sxs-lookup"><span data-stu-id="f75e5-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="f75e5-111">這個命令會建立一個 blob 範圍，該範圍會從字母順序的第一個 blob 還原到特定的 blob container2/blob2 (排除) </span><span class="sxs-lookup"><span data-stu-id="f75e5-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="f75e5-112">範例3：建立將從特定的 blob （依字母順序）到最後一個 blob (包含) 的 blob 範圍</span><span class="sxs-lookup"><span data-stu-id="f75e5-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="f75e5-113">這個命令會建立從特定的 blob container1/blob1 中還原的 blob 範圍， (包含) ，以字母順序排列到最後一個 blob。</span><span class="sxs-lookup"><span data-stu-id="f75e5-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="f75e5-114">範例4：建立將還原所有 blob 的 blob 範圍</span><span class="sxs-lookup"><span data-stu-id="f75e5-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="f75e5-115">這個命令會建立一個將還原所有 blob 的 blob 範圍。</span><span class="sxs-lookup"><span data-stu-id="f75e5-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="f75e5-116">參數</span><span class="sxs-lookup"><span data-stu-id="f75e5-116">PARAMETERS</span></span>

### <span data-ttu-id="f75e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75e5-117">-DefaultProfile</span></span>
<span data-ttu-id="f75e5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f75e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75e5-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="f75e5-119">-EndRange</span></span>
<span data-ttu-id="f75e5-120">指定 [blob 還原] 結束範圍。</span><span class="sxs-lookup"><span data-stu-id="f75e5-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="f75e5-121">[結束範圍] 會在還原 blob 中排除。</span><span class="sxs-lookup"><span data-stu-id="f75e5-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="f75e5-122">將它設為空白 strng，以還原到結尾。</span><span class="sxs-lookup"><span data-stu-id="f75e5-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="f75e5-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="f75e5-123">-StartRange</span></span>
<span data-ttu-id="f75e5-124">指定 [blob 還原起始範圍]。</span><span class="sxs-lookup"><span data-stu-id="f75e5-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="f75e5-125">開始範圍將包含在還原 blob 中。</span><span class="sxs-lookup"><span data-stu-id="f75e5-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="f75e5-126">將它設為空白字串，即可從頭開始還原。</span><span class="sxs-lookup"><span data-stu-id="f75e5-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="f75e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75e5-127">CommonParameters</span></span>
<span data-ttu-id="f75e5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f75e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75e5-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f75e5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75e5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f75e5-130">INPUTS</span></span>

### <span data-ttu-id="f75e5-131">所有</span><span class="sxs-lookup"><span data-stu-id="f75e5-131">None</span></span>

## <span data-ttu-id="f75e5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f75e5-132">OUTPUTS</span></span>

### <span data-ttu-id="f75e5-133">PSBlobRestoreRange 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f75e5-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="f75e5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f75e5-134">NOTES</span></span>

## <span data-ttu-id="f75e5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f75e5-135">RELATED LINKS</span></span>