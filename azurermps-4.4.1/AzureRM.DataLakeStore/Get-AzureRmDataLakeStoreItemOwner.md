---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 5c36257050cccf217234a3b1ef6b89120e36b3c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625198"
---
# <span data-ttu-id="87396-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="87396-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="87396-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87396-102">SYNOPSIS</span></span>
<span data-ttu-id="87396-103">取得 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="87396-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87396-104">句法</span><span class="sxs-lookup"><span data-stu-id="87396-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87396-105">說明</span><span class="sxs-lookup"><span data-stu-id="87396-105">DESCRIPTION</span></span>
<span data-ttu-id="87396-106">**AzureRmDataLakeStoreItemOwner** Cmdlet 會取得 Data Lake store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="87396-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="87396-107">示例</span><span class="sxs-lookup"><span data-stu-id="87396-107">EXAMPLES</span></span>

### <span data-ttu-id="87396-108">範例1：取得目錄的擁有者</span><span class="sxs-lookup"><span data-stu-id="87396-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="87396-109">這個命令會取得 ContosoADL 帳戶之根目錄的使用者擁有者。</span><span class="sxs-lookup"><span data-stu-id="87396-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="87396-110">參數</span><span class="sxs-lookup"><span data-stu-id="87396-110">PARAMETERS</span></span>

### <span data-ttu-id="87396-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="87396-111">-Account</span></span>
<span data-ttu-id="87396-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="87396-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="87396-113">-Path</span><span class="sxs-lookup"><span data-stu-id="87396-113">-Path</span></span>
<span data-ttu-id="87396-114">指定專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="87396-114">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="87396-115">-類型</span><span class="sxs-lookup"><span data-stu-id="87396-115">-Type</span></span>
<span data-ttu-id="87396-116">指定要取得的擁有者類型。</span><span class="sxs-lookup"><span data-stu-id="87396-116">Specifies the type of owner to get.</span></span>
<span data-ttu-id="87396-117">此參數可接受的值為： [使用者] 和 [群組]。</span><span class="sxs-lookup"><span data-stu-id="87396-117">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87396-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87396-118">-DefaultProfile</span></span>
<span data-ttu-id="87396-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87396-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87396-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87396-120">CommonParameters</span></span>
<span data-ttu-id="87396-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87396-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87396-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87396-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87396-123">輸入</span><span class="sxs-lookup"><span data-stu-id="87396-123">INPUTS</span></span>

## <span data-ttu-id="87396-124">輸出</span><span class="sxs-lookup"><span data-stu-id="87396-124">OUTPUTS</span></span>

### <span data-ttu-id="87396-125">字串</span><span class="sxs-lookup"><span data-stu-id="87396-125">string</span></span>
<span data-ttu-id="87396-126">指定專案的擁有者。</span><span class="sxs-lookup"><span data-stu-id="87396-126">The owner of the specified item.</span></span>

## <span data-ttu-id="87396-127">筆記</span><span class="sxs-lookup"><span data-stu-id="87396-127">NOTES</span></span>

## <span data-ttu-id="87396-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="87396-128">RELATED LINKS</span></span>

[<span data-ttu-id="87396-129">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="87396-129">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


