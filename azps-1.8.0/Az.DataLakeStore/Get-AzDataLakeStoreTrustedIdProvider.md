---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: d075c6792134536be84643d51f37b2379b63d5e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787950"
---
# <span data-ttu-id="33029-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="33029-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="33029-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33029-102">SYNOPSIS</span></span>
<span data-ttu-id="33029-103">在指定的 Data Lake Store 中取得指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="33029-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="33029-104">如果沒有指定提供者，則會列出該帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="33029-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="33029-105">句法</span><span class="sxs-lookup"><span data-stu-id="33029-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33029-106">說明</span><span class="sxs-lookup"><span data-stu-id="33029-106">DESCRIPTION</span></span>
<span data-ttu-id="33029-107">**AzDataLakeStoreTrustedIdProvider** Cmdlet 會取得指定資料 Lake store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="33029-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="33029-108">如果沒有指定提供者，則會列出該帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="33029-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="33029-109">示例</span><span class="sxs-lookup"><span data-stu-id="33029-109">EXAMPLES</span></span>

### <span data-ttu-id="33029-110">範例1：取得特定的信任身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="33029-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="33029-111">從帳戶 "ContosoADL" 傳回名為 "MyProvider" 的提供者</span><span class="sxs-lookup"><span data-stu-id="33029-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="33029-112">範例2：列出帳戶中的所有提供者</span><span class="sxs-lookup"><span data-stu-id="33029-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="33029-113">列出 [ContosoADL] 帳戶下的所有提供者</span><span class="sxs-lookup"><span data-stu-id="33029-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="33029-114">參數</span><span class="sxs-lookup"><span data-stu-id="33029-114">PARAMETERS</span></span>

### <span data-ttu-id="33029-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="33029-115">-Account</span></span>
<span data-ttu-id="33029-116">要從其檢索信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="33029-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="33029-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33029-117">-DefaultProfile</span></span>
<span data-ttu-id="33029-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="33029-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33029-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="33029-119">-Name</span></span>
<span data-ttu-id="33029-120">要檢索之信任身分識別提供者的名稱</span><span class="sxs-lookup"><span data-stu-id="33029-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="33029-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33029-121">-ResourceGroupName</span></span>
<span data-ttu-id="33029-122">要在其中檢索指定帳戶的指定信任身分識別提供者之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33029-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="33029-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33029-123">CommonParameters</span></span>
<span data-ttu-id="33029-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33029-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33029-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33029-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33029-126">輸入</span><span class="sxs-lookup"><span data-stu-id="33029-126">INPUTS</span></span>

### <span data-ttu-id="33029-127">System.object</span><span class="sxs-lookup"><span data-stu-id="33029-127">System.String</span></span>

## <span data-ttu-id="33029-128">輸出</span><span class="sxs-lookup"><span data-stu-id="33029-128">OUTPUTS</span></span>

### <span data-ttu-id="33029-129">DataLakeStoreTrustedIdProvider 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="33029-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="33029-130">筆記</span><span class="sxs-lookup"><span data-stu-id="33029-130">NOTES</span></span>

## <span data-ttu-id="33029-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="33029-131">RELATED LINKS</span></span>
