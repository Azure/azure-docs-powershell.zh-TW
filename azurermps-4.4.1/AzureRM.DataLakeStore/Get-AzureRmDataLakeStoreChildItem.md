---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 51b27c5dcffc36e45946d9fd2b0c842cfe17cdaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625203"
---
# <span data-ttu-id="f8f79-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="f8f79-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="f8f79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8f79-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f79-103">取得 Data Lake Store 中資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="f8f79-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f79-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8f79-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f79-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8f79-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f79-106">**AzureRmDataLakeStoreChildItem** Cmdlet 會取得 Data Lake store 中資料夾中的專案清單。</span><span class="sxs-lookup"><span data-stu-id="f8f79-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="f8f79-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8f79-107">EXAMPLES</span></span>

### <span data-ttu-id="f8f79-108">範例1：取得資料夾的子專案</span><span class="sxs-lookup"><span data-stu-id="f8f79-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="f8f79-109">這個命令會取得 MyFiles 資料夾的子專案。</span><span class="sxs-lookup"><span data-stu-id="f8f79-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="f8f79-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8f79-110">PARAMETERS</span></span>

### <span data-ttu-id="f8f79-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f8f79-111">-Account</span></span>
<span data-ttu-id="f8f79-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f8f79-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f8f79-113">-Path</span><span class="sxs-lookup"><span data-stu-id="f8f79-113">-Path</span></span>
<span data-ttu-id="f8f79-114">指定資料夾的 Data Lake Store 路徑，從 root 目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="f8f79-114">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f79-115">-DefaultProfile</span></span>
<span data-ttu-id="f8f79-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8f79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f79-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f79-117">CommonParameters</span></span>
<span data-ttu-id="f8f79-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8f79-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f79-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8f79-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f79-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f8f79-120">INPUTS</span></span>

## <span data-ttu-id="f8f79-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f8f79-121">OUTPUTS</span></span>

### <span data-ttu-id="f8f79-122">IEnumerable<DataLakeStoreItem></span><span class="sxs-lookup"><span data-stu-id="f8f79-122">IEnumerable<DataLakeStoreItem></span></span>
<span data-ttu-id="f8f79-123">在指定路徑下的 Data Lake Store 檔案和資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="f8f79-123">The list of Data Lake Store files and folders under the specified path.</span></span>

## <span data-ttu-id="f8f79-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f8f79-124">NOTES</span></span>

## <span data-ttu-id="f8f79-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8f79-125">RELATED LINKS</span></span>

