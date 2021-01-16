---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279168"
---
# <span data-ttu-id="0f469-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f469-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="0f469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f469-102">SYNOPSIS</span></span>
<span data-ttu-id="0f469-103">取得 Data Lake Store 中檔案或資料夾的許可權八進位數。</span><span class="sxs-lookup"><span data-stu-id="0f469-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0f469-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f469-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f469-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f469-105">DESCRIPTION</span></span>
<span data-ttu-id="0f469-106">**AzDataLakeStoreItemPermission** Cmdlet 會取得 Data Lake store 中檔案或資料夾的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="0f469-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0f469-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f469-107">EXAMPLES</span></span>

### <span data-ttu-id="0f469-108">範例1：設定檔案的許可權八進位</span><span class="sxs-lookup"><span data-stu-id="0f469-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="0f469-109">這個命令會取得檔案的許可權八進位。</span><span class="sxs-lookup"><span data-stu-id="0f469-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="0f469-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f469-110">PARAMETERS</span></span>

### <span data-ttu-id="0f469-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="0f469-111">-Account</span></span>
<span data-ttu-id="0f469-112">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0f469-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="0f469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f469-113">-DefaultProfile</span></span>
<span data-ttu-id="0f469-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f469-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f469-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0f469-115">-Path</span></span>
<span data-ttu-id="0f469-116">指定檔案或資料夾的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="0f469-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0f469-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f469-117">CommonParameters</span></span>
<span data-ttu-id="0f469-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f469-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f469-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f469-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f469-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0f469-120">INPUTS</span></span>

### <span data-ttu-id="0f469-121">System.object</span><span class="sxs-lookup"><span data-stu-id="0f469-121">System.String</span></span>

### <span data-ttu-id="0f469-122">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="0f469-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0f469-123">輸出</span><span class="sxs-lookup"><span data-stu-id="0f469-123">OUTPUTS</span></span>

### <span data-ttu-id="0f469-124">System.object</span><span class="sxs-lookup"><span data-stu-id="0f469-124">System.String</span></span>

## <span data-ttu-id="0f469-125">筆記</span><span class="sxs-lookup"><span data-stu-id="0f469-125">NOTES</span></span>
* <span data-ttu-id="0f469-126">別名： Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f469-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="0f469-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f469-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f469-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0f469-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


