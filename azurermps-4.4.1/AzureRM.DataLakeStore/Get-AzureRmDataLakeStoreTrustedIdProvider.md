---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: e95fd5e487fc29a40e48484b0a905def8356e260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453551"
---
# <span data-ttu-id="20557-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="20557-101">Get-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="20557-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20557-102">SYNOPSIS</span></span>
<span data-ttu-id="20557-103">在指定的 Data Lake Store 中取得指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="20557-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="20557-104">如果沒有指定提供者，則會列出該帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="20557-104">If no provider is specified, then lists all providers for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20557-105">句法</span><span class="sxs-lookup"><span data-stu-id="20557-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20557-106">說明</span><span class="sxs-lookup"><span data-stu-id="20557-106">DESCRIPTION</span></span>
<span data-ttu-id="20557-107">**AzureRmDataLakeStoreTrustedIdProvider** Cmdlet 會取得指定資料 Lake store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="20557-107">The **Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="20557-108">如果沒有指定提供者，則會列出該帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="20557-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="20557-109">示例</span><span class="sxs-lookup"><span data-stu-id="20557-109">EXAMPLES</span></span>

### <span data-ttu-id="20557-110">範例1：取得特定的信任身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="20557-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="20557-111">從帳戶 "ContosoADL" 傳回名為 "MyProvider" 的提供者</span><span class="sxs-lookup"><span data-stu-id="20557-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="20557-112">範例2：列出帳戶中的所有提供者</span><span class="sxs-lookup"><span data-stu-id="20557-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="20557-113">列出 [ContosoADL] 帳戶下的所有提供者</span><span class="sxs-lookup"><span data-stu-id="20557-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="20557-114">參數</span><span class="sxs-lookup"><span data-stu-id="20557-114">PARAMETERS</span></span>

### <span data-ttu-id="20557-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="20557-115">-Account</span></span>
<span data-ttu-id="20557-116">要從其檢索信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="20557-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="20557-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="20557-117">-Name</span></span>
<span data-ttu-id="20557-118">要檢索之信任身分識別提供者的名稱</span><span class="sxs-lookup"><span data-stu-id="20557-118">The name of the trusted identity provider to retrieve</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20557-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20557-119">-ResourceGroupName</span></span>
<span data-ttu-id="20557-120">要在其中檢索指定帳戶的指定信任身分識別提供者之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="20557-120">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20557-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20557-121">-DefaultProfile</span></span>
<span data-ttu-id="20557-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20557-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20557-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20557-123">CommonParameters</span></span>
<span data-ttu-id="20557-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20557-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20557-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20557-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20557-126">輸入</span><span class="sxs-lookup"><span data-stu-id="20557-126">INPUTS</span></span>

## <span data-ttu-id="20557-127">輸出</span><span class="sxs-lookup"><span data-stu-id="20557-127">OUTPUTS</span></span>

### <span data-ttu-id="20557-128">DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="20557-128">DataLakeStoreTrustedIdProvider</span></span>
<span data-ttu-id="20557-129">指定信任身分識別提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="20557-129">The details of the specified trusted identity provider.</span></span>

### <span data-ttu-id="20557-130">IList<DataLakeStoreTrustedIdProvider></span><span class="sxs-lookup"><span data-stu-id="20557-130">IList<DataLakeStoreTrustedIdProvider></span></span>
<span data-ttu-id="20557-131">指定帳戶中受信任身分識別提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="20557-131">The list of trusted identity providers in the specified account.</span></span>

## <span data-ttu-id="20557-132">筆記</span><span class="sxs-lookup"><span data-stu-id="20557-132">NOTES</span></span>

## <span data-ttu-id="20557-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="20557-133">RELATED LINKS</span></span>

