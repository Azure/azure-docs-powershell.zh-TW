---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: 845fbb645ca9ba3495aa0dcf2b56cdbd793630e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904697"
---
# <span data-ttu-id="117b5-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="117b5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="117b5-102">SYNOPSIS</span></span>
<span data-ttu-id="117b5-103">獲得 Data Lake Store 帳戶的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="117b5-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="117b5-104">語法</span><span class="sxs-lookup"><span data-stu-id="117b5-104">SYNTAX</span></span>

### <span data-ttu-id="117b5-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="117b5-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="117b5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="117b5-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="117b5-107">GetByS0ificAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117b5-108">描述</span><span class="sxs-lookup"><span data-stu-id="117b5-108">DESCRIPTION</span></span>
<span data-ttu-id="117b5-109">**Get-AzDataLakeStoreAccount** Cmdlet 會取得 Data Lake Store 帳戶的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="117b5-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="117b5-110">例子</span><span class="sxs-lookup"><span data-stu-id="117b5-110">EXAMPLES</span></span>

### <span data-ttu-id="117b5-111">範例 1：取得 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="117b5-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="117b5-112">此命令會獲得名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="117b5-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="117b5-113">參數</span><span class="sxs-lookup"><span data-stu-id="117b5-113">PARAMETERS</span></span>

### <span data-ttu-id="117b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117b5-114">-DefaultProfile</span></span>
<span data-ttu-id="117b5-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="117b5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="117b5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="117b5-116">-Name</span></span>
<span data-ttu-id="117b5-117">指定要取得的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="117b5-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="117b5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117b5-118">-ResourceGroupName</span></span>
<span data-ttu-id="117b5-119">指定包含要取得 Data Lake 市集帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="117b5-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="117b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117b5-120">CommonParameters</span></span>
<span data-ttu-id="117b5-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="117b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117b5-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="117b5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117b5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="117b5-123">INPUTS</span></span>

### <span data-ttu-id="117b5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="117b5-124">System.String</span></span>

## <span data-ttu-id="117b5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="117b5-125">OUTPUTS</span></span>

### <span data-ttu-id="117b5-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="117b5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="117b5-127">NOTES</span></span>

## <span data-ttu-id="117b5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="117b5-128">RELATED LINKS</span></span>

[<span data-ttu-id="117b5-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="117b5-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="117b5-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="117b5-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="117b5-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


