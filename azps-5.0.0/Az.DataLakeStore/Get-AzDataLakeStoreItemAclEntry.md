---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285054"
---
# <span data-ttu-id="e8592-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e8592-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="e8592-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8592-102">SYNOPSIS</span></span>
<span data-ttu-id="e8592-103">在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="e8592-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e8592-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8592-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8592-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8592-105">DESCRIPTION</span></span>
<span data-ttu-id="e8592-106">**AzDataLakeStoreItemAclEntry** Cmdlet 會取得)  (資料 Lake store 中檔案或資料夾的存取控制清單中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="e8592-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e8592-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8592-107">EXAMPLES</span></span>

### <span data-ttu-id="e8592-108">範例1：取得資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="e8592-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="e8592-109">這個命令會取得指定資料 Lake Store 帳戶之根目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="e8592-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="e8592-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8592-110">PARAMETERS</span></span>

### <span data-ttu-id="e8592-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e8592-111">-Account</span></span>
<span data-ttu-id="e8592-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8592-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8592-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8592-113">-DefaultProfile</span></span>
<span data-ttu-id="e8592-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8592-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8592-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e8592-115">-Path</span></span>
<span data-ttu-id="e8592-116">指定此 Cmdlet 取得 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="e8592-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8592-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8592-117">CommonParameters</span></span>
<span data-ttu-id="e8592-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8592-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8592-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8592-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8592-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e8592-120">INPUTS</span></span>

### <span data-ttu-id="e8592-121">System.object</span><span class="sxs-lookup"><span data-stu-id="e8592-121">System.String</span></span>

### <span data-ttu-id="e8592-122">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="e8592-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="e8592-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e8592-123">OUTPUTS</span></span>

### <span data-ttu-id="e8592-124">DataLakeStoreItemAce 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="e8592-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="e8592-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e8592-125">NOTES</span></span>

## <span data-ttu-id="e8592-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8592-126">RELATED LINKS</span></span>

[<span data-ttu-id="e8592-127">移除-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e8592-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="e8592-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e8592-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


