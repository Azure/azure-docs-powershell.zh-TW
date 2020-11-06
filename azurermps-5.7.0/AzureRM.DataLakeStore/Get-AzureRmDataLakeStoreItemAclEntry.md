---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 0e1182843ee57809fe3c6a0ed1c7f516678fc1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448689"
---
# <span data-ttu-id="310e3-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="310e3-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="310e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="310e3-102">SYNOPSIS</span></span>
<span data-ttu-id="310e3-103">在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="310e3-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="310e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="310e3-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="310e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="310e3-105">DESCRIPTION</span></span>
<span data-ttu-id="310e3-106">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會取得)  (資料 Lake store 中檔案或資料夾的存取控制清單中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="310e3-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="310e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="310e3-107">EXAMPLES</span></span>

### <span data-ttu-id="310e3-108">範例1：取得資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="310e3-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="310e3-109">這個命令會取得指定資料 Lake Store 帳戶之根目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="310e3-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="310e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="310e3-110">PARAMETERS</span></span>

### <span data-ttu-id="310e3-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="310e3-111">-Account</span></span>
<span data-ttu-id="310e3-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="310e3-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="310e3-113">-DefaultProfile</span></span>
<span data-ttu-id="310e3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="310e3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="310e3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="310e3-115">-Path</span></span>
<span data-ttu-id="310e3-116">指定此 Cmdlet 取得 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="310e3-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="310e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="310e3-117">CommonParameters</span></span>
<span data-ttu-id="310e3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="310e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="310e3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="310e3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="310e3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="310e3-120">INPUTS</span></span>

### <span data-ttu-id="310e3-121">所有</span><span class="sxs-lookup"><span data-stu-id="310e3-121">None</span></span>
<span data-ttu-id="310e3-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="310e3-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="310e3-123">輸出</span><span class="sxs-lookup"><span data-stu-id="310e3-123">OUTPUTS</span></span>

### <span data-ttu-id="310e3-124">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="310e3-124">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="310e3-125">指定資料夾或檔案的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="310e3-125">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="310e3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="310e3-126">NOTES</span></span>

## <span data-ttu-id="310e3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="310e3-127">RELATED LINKS</span></span>

[<span data-ttu-id="310e3-128">移除-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="310e3-128">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="310e3-129">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="310e3-129">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


