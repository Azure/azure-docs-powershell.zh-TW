---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625199"
---
# <span data-ttu-id="c51a2-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c51a2-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="c51a2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c51a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c51a2-103">在 Data Lake Store 中取得檔案或資料夾的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="c51a2-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c51a2-104">句法</span><span class="sxs-lookup"><span data-stu-id="c51a2-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c51a2-105">說明</span><span class="sxs-lookup"><span data-stu-id="c51a2-105">DESCRIPTION</span></span>
<span data-ttu-id="c51a2-106">**AzureRmDataLakeStoreItemAclEntry** Cmdlet 會取得)  (資料 Lake store 中檔案或資料夾的存取控制清單中 (ACE) 的專案。</span><span class="sxs-lookup"><span data-stu-id="c51a2-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c51a2-107">示例</span><span class="sxs-lookup"><span data-stu-id="c51a2-107">EXAMPLES</span></span>

### <span data-ttu-id="c51a2-108">範例1：取得資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="c51a2-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="c51a2-109">這個命令會取得指定資料 Lake Store 帳戶之根目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="c51a2-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="c51a2-110">參數</span><span class="sxs-lookup"><span data-stu-id="c51a2-110">PARAMETERS</span></span>

### <span data-ttu-id="c51a2-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="c51a2-111">-Account</span></span>
<span data-ttu-id="c51a2-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c51a2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c51a2-113">-Path</span><span class="sxs-lookup"><span data-stu-id="c51a2-113">-Path</span></span>
<span data-ttu-id="c51a2-114">指定此 Cmdlet 取得 ACE 的專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="c51a2-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c51a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51a2-115">-DefaultProfile</span></span>
<span data-ttu-id="c51a2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c51a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c51a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51a2-117">CommonParameters</span></span>
<span data-ttu-id="c51a2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c51a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51a2-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c51a2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51a2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c51a2-120">INPUTS</span></span>

## <span data-ttu-id="c51a2-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c51a2-121">OUTPUTS</span></span>

### <span data-ttu-id="c51a2-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="c51a2-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="c51a2-123">指定資料夾或檔案的 ACL 專案清單。</span><span class="sxs-lookup"><span data-stu-id="c51a2-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="c51a2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c51a2-124">NOTES</span></span>

## <span data-ttu-id="c51a2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c51a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="c51a2-126">移除-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c51a2-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="c51a2-127">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c51a2-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


