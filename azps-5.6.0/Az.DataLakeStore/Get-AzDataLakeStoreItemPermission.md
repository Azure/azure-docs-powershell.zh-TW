---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 0754160aa375ba84ac469771a97f792c36b51ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910250"
---
# <span data-ttu-id="d27c0-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d27c0-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="d27c0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d27c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d27c0-103">在 Data Lake Store 中獲得檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="d27c0-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d27c0-104">語法</span><span class="sxs-lookup"><span data-stu-id="d27c0-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d27c0-105">描述</span><span class="sxs-lookup"><span data-stu-id="d27c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d27c0-106">**Get-AzDataLakeStoreItemPermission Cmdlet** 會取得 Data Lake Store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="d27c0-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d27c0-107">例子</span><span class="sxs-lookup"><span data-stu-id="d27c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d27c0-108">範例 1：設定檔案的許可權八進位</span><span class="sxs-lookup"><span data-stu-id="d27c0-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="d27c0-109">此命令會獲得檔案的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="d27c0-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="d27c0-110">參數</span><span class="sxs-lookup"><span data-stu-id="d27c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d27c0-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d27c0-111">-Account</span></span>
<span data-ttu-id="d27c0-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d27c0-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d27c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d27c0-113">-DefaultProfile</span></span>
<span data-ttu-id="d27c0-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d27c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d27c0-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="d27c0-115">-Path</span></span>
<span data-ttu-id="d27c0-116">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="d27c0-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d27c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d27c0-117">CommonParameters</span></span>
<span data-ttu-id="d27c0-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d27c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d27c0-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d27c0-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d27c0-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d27c0-120">INPUTS</span></span>

### <span data-ttu-id="d27c0-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d27c0-121">System.String</span></span>

### <span data-ttu-id="d27c0-122">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d27c0-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d27c0-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d27c0-123">OUTPUTS</span></span>

### <span data-ttu-id="d27c0-124">System.String</span><span class="sxs-lookup"><span data-stu-id="d27c0-124">System.String</span></span>

## <span data-ttu-id="d27c0-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d27c0-125">NOTES</span></span>
* <span data-ttu-id="d27c0-126">別名：Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d27c0-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="d27c0-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d27c0-127">RELATED LINKS</span></span>

[<span data-ttu-id="d27c0-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d27c0-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


