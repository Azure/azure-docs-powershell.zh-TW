---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450639"
---
# <span data-ttu-id="d8851-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="d8851-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8851-102">SYNOPSIS</span></span>
<span data-ttu-id="d8851-103">取得 Data Lake Store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d8851-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8851-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8851-104">SYNTAX</span></span>

### <span data-ttu-id="d8851-105">GetAllInSubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="d8851-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8851-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d8851-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d8851-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8851-108">說明</span><span class="sxs-lookup"><span data-stu-id="d8851-108">DESCRIPTION</span></span>
<span data-ttu-id="d8851-109">**AzureRmDataLakeStoreAccount** Cmdlet 會取得資料 Lake store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d8851-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="d8851-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8851-110">EXAMPLES</span></span>

### <span data-ttu-id="d8851-111">範例1：取得資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="d8851-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="d8851-112">這個命令會取得名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="d8851-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="d8851-113">參數</span><span class="sxs-lookup"><span data-stu-id="d8851-113">PARAMETERS</span></span>

### <span data-ttu-id="d8851-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8851-114">-DefaultProfile</span></span>
<span data-ttu-id="d8851-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d8851-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8851-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8851-116">-Name</span></span>
<span data-ttu-id="d8851-117">指定要取得的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d8851-117">Specifies the name of the account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8851-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8851-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8851-119">指定包含要取得之 Data Lake Store 帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8851-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8851-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8851-120">CommonParameters</span></span>
<span data-ttu-id="d8851-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8851-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8851-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8851-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8851-123">輸入</span><span class="sxs-lookup"><span data-stu-id="d8851-123">INPUTS</span></span>

### <span data-ttu-id="d8851-124">所有</span><span class="sxs-lookup"><span data-stu-id="d8851-124">None</span></span>
<span data-ttu-id="d8851-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d8851-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8851-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d8851-126">OUTPUTS</span></span>

### <span data-ttu-id="d8851-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="d8851-128">要求的特定 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="d8851-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="d8851-129">清單<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="d8851-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="d8851-130">指定的資源群組或訂閱中的 Data Lake Store 帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="d8851-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="d8851-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d8851-131">NOTES</span></span>

## <span data-ttu-id="d8851-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8851-132">RELATED LINKS</span></span>

[<span data-ttu-id="d8851-133">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d8851-134">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d8851-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="d8851-136">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d8851-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


