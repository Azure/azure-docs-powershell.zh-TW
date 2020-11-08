---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: ae87c0cc6c9ccea3935e3bd0856d033895070515
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129006"
---
# <span data-ttu-id="939cd-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="939cd-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="939cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="939cd-102">SYNOPSIS</span></span>
<span data-ttu-id="939cd-103">取得 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="939cd-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="939cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="939cd-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="939cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="939cd-105">DESCRIPTION</span></span>
<span data-ttu-id="939cd-106">**AzDataLakeStoreItemOwner** Cmdlet 會取得 Data Lake store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="939cd-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="939cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="939cd-107">EXAMPLES</span></span>

### <span data-ttu-id="939cd-108">範例1：取得目錄的擁有者</span><span class="sxs-lookup"><span data-stu-id="939cd-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="939cd-109">這個命令會取得 ContosoADL 帳戶之根目錄的使用者擁有者。</span><span class="sxs-lookup"><span data-stu-id="939cd-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="939cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="939cd-110">PARAMETERS</span></span>

### <span data-ttu-id="939cd-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="939cd-111">-Account</span></span>
<span data-ttu-id="939cd-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="939cd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="939cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="939cd-113">-DefaultProfile</span></span>
<span data-ttu-id="939cd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="939cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="939cd-115">-Path</span><span class="sxs-lookup"><span data-stu-id="939cd-115">-Path</span></span>
<span data-ttu-id="939cd-116">指定專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="939cd-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="939cd-117">-類型</span><span class="sxs-lookup"><span data-stu-id="939cd-117">-Type</span></span>
<span data-ttu-id="939cd-118">指定要取得的擁有者類型。</span><span class="sxs-lookup"><span data-stu-id="939cd-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="939cd-119">此參數可接受的值為： [使用者] 和 [群組]。</span><span class="sxs-lookup"><span data-stu-id="939cd-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="939cd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="939cd-120">CommonParameters</span></span>
<span data-ttu-id="939cd-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="939cd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="939cd-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="939cd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="939cd-123">輸入</span><span class="sxs-lookup"><span data-stu-id="939cd-123">INPUTS</span></span>

### <span data-ttu-id="939cd-124">System.object</span><span class="sxs-lookup"><span data-stu-id="939cd-124">System.String</span></span>

### <span data-ttu-id="939cd-125">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="939cd-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="939cd-126">DataLakeStoreEnums + 擁有者 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="939cd-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="939cd-127">輸出</span><span class="sxs-lookup"><span data-stu-id="939cd-127">OUTPUTS</span></span>

### <span data-ttu-id="939cd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="939cd-128">System.String</span></span>

## <span data-ttu-id="939cd-129">筆記</span><span class="sxs-lookup"><span data-stu-id="939cd-129">NOTES</span></span>

## <span data-ttu-id="939cd-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="939cd-130">RELATED LINKS</span></span>

[<span data-ttu-id="939cd-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="939cd-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)

