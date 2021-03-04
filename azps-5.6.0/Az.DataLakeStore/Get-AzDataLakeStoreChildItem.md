---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: e27fde6a25fc512b898ded7d4f087ab7b344d293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903246"
---
# <span data-ttu-id="137cc-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="137cc-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="137cc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="137cc-102">SYNOPSIS</span></span>
<span data-ttu-id="137cc-103">在 Data Lake Store 中，在資料夾中獲得專案清單。</span><span class="sxs-lookup"><span data-stu-id="137cc-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="137cc-104">語法</span><span class="sxs-lookup"><span data-stu-id="137cc-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="137cc-105">描述</span><span class="sxs-lookup"><span data-stu-id="137cc-105">DESCRIPTION</span></span>
<span data-ttu-id="137cc-106">**Get-AzDataLakeStoreChildItem** Cmdlet 會取得 Data Lake Store 資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="137cc-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="137cc-107">例子</span><span class="sxs-lookup"><span data-stu-id="137cc-107">EXAMPLES</span></span>

### <span data-ttu-id="137cc-108">範例 1：取得資料夾的子專案</span><span class="sxs-lookup"><span data-stu-id="137cc-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="137cc-109">此命令會獲得 MyFiles 資料夾的子專案。</span><span class="sxs-lookup"><span data-stu-id="137cc-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="137cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="137cc-110">PARAMETERS</span></span>

### <span data-ttu-id="137cc-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="137cc-111">-Account</span></span>
<span data-ttu-id="137cc-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="137cc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="137cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137cc-113">-DefaultProfile</span></span>
<span data-ttu-id="137cc-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="137cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="137cc-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="137cc-115">-Path</span></span>
<span data-ttu-id="137cc-116">指定資料夾的 Data Lake Store 路徑，從 / (根目錄開始) 。</span><span class="sxs-lookup"><span data-stu-id="137cc-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="137cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137cc-117">CommonParameters</span></span>
<span data-ttu-id="137cc-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="137cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137cc-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="137cc-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137cc-120">輸入</span><span class="sxs-lookup"><span data-stu-id="137cc-120">INPUTS</span></span>

### <span data-ttu-id="137cc-121">System.String</span><span class="sxs-lookup"><span data-stu-id="137cc-121">System.String</span></span>

### <span data-ttu-id="137cc-122">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="137cc-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="137cc-123">輸出</span><span class="sxs-lookup"><span data-stu-id="137cc-123">OUTPUTS</span></span>

### <span data-ttu-id="137cc-124">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="137cc-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="137cc-125">筆記</span><span class="sxs-lookup"><span data-stu-id="137cc-125">NOTES</span></span>

## <span data-ttu-id="137cc-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="137cc-126">RELATED LINKS</span></span>
