---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 654703a3c5cf1fc18e0f8fbb227b608e91c379bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910717"
---
# <span data-ttu-id="23500-101">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="23500-101">Get-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="23500-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23500-102">SYNOPSIS</span></span>
<span data-ttu-id="23500-103">在 Data Lake Store 中，獲得檔案或資料夾的擁有者。</span><span class="sxs-lookup"><span data-stu-id="23500-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="23500-104">語法</span><span class="sxs-lookup"><span data-stu-id="23500-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23500-105">描述</span><span class="sxs-lookup"><span data-stu-id="23500-105">DESCRIPTION</span></span>
<span data-ttu-id="23500-106">**Get-AzDataLakeStoreItem Ownerer Cmdlet** 會取得 Data Lake Store 中檔案或資料夾的擁有者。</span><span class="sxs-lookup"><span data-stu-id="23500-106">The **Get-AzDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="23500-107">例子</span><span class="sxs-lookup"><span data-stu-id="23500-107">EXAMPLES</span></span>

### <span data-ttu-id="23500-108">範例 1：取得目錄的擁有者</span><span class="sxs-lookup"><span data-stu-id="23500-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="23500-109">此命令會獲得 ContosoADL 帳戶根目錄的使用者擁有者。</span><span class="sxs-lookup"><span data-stu-id="23500-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="23500-110">參數</span><span class="sxs-lookup"><span data-stu-id="23500-110">PARAMETERS</span></span>

### <span data-ttu-id="23500-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="23500-111">-Account</span></span>
<span data-ttu-id="23500-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="23500-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="23500-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23500-113">-DefaultProfile</span></span>
<span data-ttu-id="23500-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23500-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23500-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="23500-115">-Path</span></span>
<span data-ttu-id="23500-116">指定專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="23500-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="23500-117">-類型</span><span class="sxs-lookup"><span data-stu-id="23500-117">-Type</span></span>
<span data-ttu-id="23500-118">指定要取得之擁有者的類型。</span><span class="sxs-lookup"><span data-stu-id="23500-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="23500-119">此參數可接受的值為：使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="23500-119">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="23500-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23500-120">CommonParameters</span></span>
<span data-ttu-id="23500-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23500-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23500-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="23500-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23500-123">輸入</span><span class="sxs-lookup"><span data-stu-id="23500-123">INPUTS</span></span>

### <span data-ttu-id="23500-124">System.String</span><span class="sxs-lookup"><span data-stu-id="23500-124">System.String</span></span>

### <span data-ttu-id="23500-125">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="23500-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="23500-126">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="23500-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="23500-127">輸出</span><span class="sxs-lookup"><span data-stu-id="23500-127">OUTPUTS</span></span>

### <span data-ttu-id="23500-128">System.String</span><span class="sxs-lookup"><span data-stu-id="23500-128">System.String</span></span>

## <span data-ttu-id="23500-129">筆記</span><span class="sxs-lookup"><span data-stu-id="23500-129">NOTES</span></span>

## <span data-ttu-id="23500-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="23500-130">RELATED LINKS</span></span>

[<span data-ttu-id="23500-131">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="23500-131">Set-AzDataLakeStoreItemOwner</span></span>](./Set-AzDataLakeStoreItemOwner.md)


