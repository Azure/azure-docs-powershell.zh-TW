---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 76d745c16dae7fdfae7feca46c3b32715fa82f5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912873"
---
# <span data-ttu-id="d0ffd-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d0ffd-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="d0ffd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ffd-103">在 Data Lake Store 中，在檔案或資料夾的 ACL 中輸入專案。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d0ffd-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0ffd-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ffd-105">描述</span><span class="sxs-lookup"><span data-stu-id="d0ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="d0ffd-106">**Get-AzDataLakeStoreItemAclEntry Cmdlet** 會取得資料湖市集檔案或資料夾存取控制清單 (ACL) 中的專案 (ACE) 。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d0ffd-107">例子</span><span class="sxs-lookup"><span data-stu-id="d0ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="d0ffd-108">範例 1：取得資料夾的 ACL</span><span class="sxs-lookup"><span data-stu-id="d0ffd-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="d0ffd-109">此命令會獲得指定 Data Lake Store 帳戶根目錄的 ACL</span><span class="sxs-lookup"><span data-stu-id="d0ffd-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="d0ffd-110">參數</span><span class="sxs-lookup"><span data-stu-id="d0ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="d0ffd-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d0ffd-111">-Account</span></span>
<span data-ttu-id="d0ffd-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d0ffd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ffd-113">-DefaultProfile</span></span>
<span data-ttu-id="d0ffd-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0ffd-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="d0ffd-115">-Path</span></span>
<span data-ttu-id="d0ffd-116">指定此 Cmdlet 會獲得 ACE 之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d0ffd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ffd-117">CommonParameters</span></span>
<span data-ttu-id="d0ffd-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ffd-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d0ffd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ffd-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d0ffd-120">INPUTS</span></span>

### <span data-ttu-id="d0ffd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d0ffd-121">System.String</span></span>

### <span data-ttu-id="d0ffd-122">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d0ffd-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d0ffd-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d0ffd-123">OUTPUTS</span></span>

### <span data-ttu-id="d0ffd-124">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="d0ffd-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="d0ffd-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d0ffd-125">NOTES</span></span>

## <span data-ttu-id="d0ffd-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0ffd-126">RELATED LINKS</span></span>

[<span data-ttu-id="d0ffd-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d0ffd-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="d0ffd-128">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d0ffd-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


