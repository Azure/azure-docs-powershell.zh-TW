---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: ac03d161e8ea786b939f8068dc2efd9109af3ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906709"
---
# <span data-ttu-id="a236c-101">Get-AzDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a236c-101">Get-AzDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a236c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a236c-102">SYNOPSIS</span></span>
<span data-ttu-id="a236c-103">在指定的 Data Lake Store 中，獲得指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="a236c-103">Gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="a236c-104">如果沒有指定提供者，請列出帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="a236c-104">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="a236c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a236c-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a236c-106">描述</span><span class="sxs-lookup"><span data-stu-id="a236c-106">DESCRIPTION</span></span>
<span data-ttu-id="a236c-107">**Get-AzDataLakeStoreTrustedIdProvider Cmdlet** 會取得指定 Data Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="a236c-107">The **Get-AzDataLakeStoreTrustedIdProvider** cmdlet gets the specified trusted identity provider in the specified Data Lake Store.</span></span>
<span data-ttu-id="a236c-108">如果沒有指定提供者，請列出帳戶的所有提供者。</span><span class="sxs-lookup"><span data-stu-id="a236c-108">If no provider is specified, then lists all providers for the account.</span></span>

## <span data-ttu-id="a236c-109">例子</span><span class="sxs-lookup"><span data-stu-id="a236c-109">EXAMPLES</span></span>

### <span data-ttu-id="a236c-110">範例 1：取得特定的信任身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="a236c-110">Example 1: Get a specific trusted identity provider</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="a236c-111">從帳戶 "ContosoADL" 將提供者命名為 "MyProvider"</span><span class="sxs-lookup"><span data-stu-id="a236c-111">Returns the provider named "MyProvider" from account "ContosoADL"</span></span>

### <span data-ttu-id="a236c-112">範例 2：列出帳戶中的所有提供者</span><span class="sxs-lookup"><span data-stu-id="a236c-112">Example 2: List all providers in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

<span data-ttu-id="a236c-113">在帳戶 "ContosoADL" 下列出所有提供者</span><span class="sxs-lookup"><span data-stu-id="a236c-113">Lists all providers under the account "ContosoADL"</span></span>

## <span data-ttu-id="a236c-114">參數</span><span class="sxs-lookup"><span data-stu-id="a236c-114">PARAMETERS</span></span>

### <span data-ttu-id="a236c-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a236c-115">-Account</span></span>
<span data-ttu-id="a236c-116">Data Lake Store 帳戶以從</span><span class="sxs-lookup"><span data-stu-id="a236c-116">The Data Lake Store account to retrieve the trusted identity provider from</span></span>

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

### <span data-ttu-id="a236c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a236c-117">-DefaultProfile</span></span>
<span data-ttu-id="a236c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a236c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a236c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="a236c-119">-Name</span></span>
<span data-ttu-id="a236c-120">要取回的受信任身分識別提供者名稱</span><span class="sxs-lookup"><span data-stu-id="a236c-120">The name of the trusted identity provider to retrieve</span></span>

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

### <span data-ttu-id="a236c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a236c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a236c-122">資源組的名稱，其下想要取回指定帳戶的指定信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="a236c-122">Name of resource group under which want to retrieve the specified account's specified trusted identity provider.</span></span>

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

### <span data-ttu-id="a236c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a236c-123">CommonParameters</span></span>
<span data-ttu-id="a236c-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a236c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a236c-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a236c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a236c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a236c-126">INPUTS</span></span>

### <span data-ttu-id="a236c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a236c-127">System.String</span></span>

## <span data-ttu-id="a236c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a236c-128">OUTPUTS</span></span>

### <span data-ttu-id="a236c-129">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="a236c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="a236c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a236c-130">NOTES</span></span>

## <span data-ttu-id="a236c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a236c-131">RELATED LINKS</span></span>
