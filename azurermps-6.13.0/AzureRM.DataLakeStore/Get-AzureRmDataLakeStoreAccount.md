---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443892"
---
# <span data-ttu-id="68a05-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="68a05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68a05-102">SYNOPSIS</span></span>
<span data-ttu-id="68a05-103">取得 Data Lake Store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="68a05-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68a05-104">句法</span><span class="sxs-lookup"><span data-stu-id="68a05-104">SYNTAX</span></span>

### <span data-ttu-id="68a05-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="68a05-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68a05-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68a05-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68a05-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68a05-108">說明</span><span class="sxs-lookup"><span data-stu-id="68a05-108">DESCRIPTION</span></span>
<span data-ttu-id="68a05-109">**AzureRmDataLakeStoreAccount** Cmdlet 會取得資料 Lake store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="68a05-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="68a05-110">示例</span><span class="sxs-lookup"><span data-stu-id="68a05-110">EXAMPLES</span></span>

### <span data-ttu-id="68a05-111">範例1：取得資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="68a05-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="68a05-112">這個命令會取得名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="68a05-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="68a05-113">參數</span><span class="sxs-lookup"><span data-stu-id="68a05-113">PARAMETERS</span></span>

### <span data-ttu-id="68a05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a05-114">-DefaultProfile</span></span>
<span data-ttu-id="68a05-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="68a05-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68a05-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="68a05-116">-Name</span></span>
<span data-ttu-id="68a05-117">指定要取得的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="68a05-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="68a05-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a05-118">-ResourceGroupName</span></span>
<span data-ttu-id="68a05-119">指定包含要取得之 Data Lake Store 帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68a05-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="68a05-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a05-120">CommonParameters</span></span>
<span data-ttu-id="68a05-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68a05-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a05-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68a05-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a05-123">輸入</span><span class="sxs-lookup"><span data-stu-id="68a05-123">INPUTS</span></span>

### <span data-ttu-id="68a05-124">System.object</span><span class="sxs-lookup"><span data-stu-id="68a05-124">System.String</span></span>

## <span data-ttu-id="68a05-125">輸出</span><span class="sxs-lookup"><span data-stu-id="68a05-125">OUTPUTS</span></span>

### <span data-ttu-id="68a05-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="68a05-127">筆記</span><span class="sxs-lookup"><span data-stu-id="68a05-127">NOTES</span></span>

## <span data-ttu-id="68a05-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="68a05-128">RELATED LINKS</span></span>

[<span data-ttu-id="68a05-129">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="68a05-130">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="68a05-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="68a05-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="68a05-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


