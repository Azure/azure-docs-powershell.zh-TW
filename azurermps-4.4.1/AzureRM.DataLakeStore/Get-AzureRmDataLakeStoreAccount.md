---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: c05ca64db5b04ef78778e39d9ae6347db4ca05b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446820"
---
# <span data-ttu-id="0d897-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="0d897-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d897-102">SYNOPSIS</span></span>
<span data-ttu-id="0d897-103">取得 Data Lake Store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0d897-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d897-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d897-104">SYNTAX</span></span>

### <span data-ttu-id="0d897-105">[全部在訂閱] 中 (預設) </span><span class="sxs-lookup"><span data-stu-id="0d897-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d897-106">[資源群組] 中的 [全部]</span><span class="sxs-lookup"><span data-stu-id="0d897-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d897-107">特定帳戶</span><span class="sxs-lookup"><span data-stu-id="0d897-107">Specific Account</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d897-108">說明</span><span class="sxs-lookup"><span data-stu-id="0d897-108">DESCRIPTION</span></span>
<span data-ttu-id="0d897-109">**AzureRmDataLakeStoreAccount** Cmdlet 會取得資料 Lake store 帳戶的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0d897-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="0d897-110">示例</span><span class="sxs-lookup"><span data-stu-id="0d897-110">EXAMPLES</span></span>

### <span data-ttu-id="0d897-111">範例1：取得資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="0d897-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="0d897-112">這個命令會取得名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="0d897-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="0d897-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d897-113">PARAMETERS</span></span>

### <span data-ttu-id="0d897-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d897-114">-Name</span></span>
<span data-ttu-id="0d897-115">指定要取得的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0d897-115">Specifies the name of the account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d897-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d897-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d897-117">指定包含要取得之 Data Lake Store 帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d897-117">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d897-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d897-118">-DefaultProfile</span></span>
<span data-ttu-id="0d897-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d897-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d897-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d897-120">CommonParameters</span></span>
<span data-ttu-id="0d897-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d897-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d897-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d897-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d897-123">輸入</span><span class="sxs-lookup"><span data-stu-id="0d897-123">INPUTS</span></span>

## <span data-ttu-id="0d897-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0d897-124">OUTPUTS</span></span>

### <span data-ttu-id="0d897-125">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-125">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="0d897-126">要求的特定 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="0d897-126">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="0d897-127">清單<PSDataLakeStoreAccount></span><span class="sxs-lookup"><span data-stu-id="0d897-127">List<PSDataLakeStoreAccount></span></span>
<span data-ttu-id="0d897-128">指定的資源群組或訂閱中的 Data Lake Store 帳戶清單。</span><span class="sxs-lookup"><span data-stu-id="0d897-128">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="0d897-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0d897-129">NOTES</span></span>

## <span data-ttu-id="0d897-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d897-130">RELATED LINKS</span></span>

[<span data-ttu-id="0d897-131">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0d897-132">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-132">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0d897-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="0d897-134">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0d897-134">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


