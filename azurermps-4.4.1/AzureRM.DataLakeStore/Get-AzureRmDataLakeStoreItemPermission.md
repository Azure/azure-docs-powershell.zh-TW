---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453548"
---
# <span data-ttu-id="b09df-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b09df-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="b09df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b09df-102">SYNOPSIS</span></span>
<span data-ttu-id="b09df-103">取得 Data Lake Store 中檔案或資料夾的許可權八進位數。</span><span class="sxs-lookup"><span data-stu-id="b09df-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b09df-104">句法</span><span class="sxs-lookup"><span data-stu-id="b09df-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b09df-105">說明</span><span class="sxs-lookup"><span data-stu-id="b09df-105">DESCRIPTION</span></span>
<span data-ttu-id="b09df-106">**AzureRmDataLakeStoreItemPermission** Cmdlet 會取得 Data Lake store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="b09df-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b09df-107">示例</span><span class="sxs-lookup"><span data-stu-id="b09df-107">EXAMPLES</span></span>

### <span data-ttu-id="b09df-108">範例1：設定檔案的許可權八進位</span><span class="sxs-lookup"><span data-stu-id="b09df-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="b09df-109">這個命令會取得檔案的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="b09df-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="b09df-110">參數</span><span class="sxs-lookup"><span data-stu-id="b09df-110">PARAMETERS</span></span>

### <span data-ttu-id="b09df-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b09df-111">-Account</span></span>
<span data-ttu-id="b09df-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b09df-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="b09df-113">-Path</span><span class="sxs-lookup"><span data-stu-id="b09df-113">-Path</span></span>
<span data-ttu-id="b09df-114">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="b09df-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b09df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09df-115">-DefaultProfile</span></span>
<span data-ttu-id="b09df-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b09df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b09df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09df-117">CommonParameters</span></span>
<span data-ttu-id="b09df-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b09df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09df-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b09df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09df-120">輸入</span><span class="sxs-lookup"><span data-stu-id="b09df-120">INPUTS</span></span>

## <span data-ttu-id="b09df-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b09df-121">OUTPUTS</span></span>

### <span data-ttu-id="b09df-122">字串</span><span class="sxs-lookup"><span data-stu-id="b09df-122">string</span></span>
<span data-ttu-id="b09df-123">擁有權的字串標記法（八進位）</span><span class="sxs-lookup"><span data-stu-id="b09df-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="b09df-124">筆記</span><span class="sxs-lookup"><span data-stu-id="b09df-124">NOTES</span></span>
* <span data-ttu-id="b09df-125">別名： Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b09df-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="b09df-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b09df-126">RELATED LINKS</span></span>

[<span data-ttu-id="b09df-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="b09df-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


