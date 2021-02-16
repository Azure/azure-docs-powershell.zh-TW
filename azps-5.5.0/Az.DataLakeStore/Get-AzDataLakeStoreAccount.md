---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 2874bfc6e866e1e9af37b5a66545ec72c5c4f24c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133314"
---
# <span data-ttu-id="3a87d-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="3a87d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a87d-102">SYNOPSIS</span></span>
<span data-ttu-id="3a87d-103">取得 Data Lake Store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a87d-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="3a87d-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a87d-104">SYNTAX</span></span>

### <span data-ttu-id="3a87d-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="3a87d-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a87d-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a87d-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a87d-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a87d-108">說明</span><span class="sxs-lookup"><span data-stu-id="3a87d-108">DESCRIPTION</span></span>
<span data-ttu-id="3a87d-109">**AzDataLakeStoreAccount** Cmdlet 會取得資料 Lake store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3a87d-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="3a87d-110">示例</span><span class="sxs-lookup"><span data-stu-id="3a87d-110">EXAMPLES</span></span>

### <span data-ttu-id="3a87d-111">範例1：取得資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="3a87d-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="3a87d-112">這個命令會取得名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="3a87d-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="3a87d-113">參數</span><span class="sxs-lookup"><span data-stu-id="3a87d-113">PARAMETERS</span></span>

### <span data-ttu-id="3a87d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a87d-114">-DefaultProfile</span></span>
<span data-ttu-id="3a87d-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3a87d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a87d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a87d-116">-Name</span></span>
<span data-ttu-id="3a87d-117">指定要取得的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3a87d-117">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a87d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a87d-118">-ResourceGroupName</span></span>
<span data-ttu-id="3a87d-119">指定包含要取得之 Data Lake Store 帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a87d-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a87d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a87d-120">CommonParameters</span></span>
<span data-ttu-id="3a87d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a87d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a87d-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3a87d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a87d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="3a87d-123">INPUTS</span></span>

### <span data-ttu-id="3a87d-124">System.object</span><span class="sxs-lookup"><span data-stu-id="3a87d-124">System.String</span></span>

## <span data-ttu-id="3a87d-125">輸出</span><span class="sxs-lookup"><span data-stu-id="3a87d-125">OUTPUTS</span></span>

### <span data-ttu-id="3a87d-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="3a87d-127">筆記</span><span class="sxs-lookup"><span data-stu-id="3a87d-127">NOTES</span></span>

## <span data-ttu-id="3a87d-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a87d-128">RELATED LINKS</span></span>

[<span data-ttu-id="3a87d-129">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3a87d-130">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3a87d-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3a87d-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3a87d-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


