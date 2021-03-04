---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bc8a09add012cb0f190922777e2e9e7fcc46feb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913217"
---
# <span data-ttu-id="daf5e-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="daf5e-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="daf5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="daf5e-102">SYNOPSIS</span></span>
<span data-ttu-id="daf5e-103">測試 Data Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="daf5e-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="daf5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="daf5e-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf5e-105">描述</span><span class="sxs-lookup"><span data-stu-id="daf5e-105">DESCRIPTION</span></span>
<span data-ttu-id="daf5e-106">**Test-AzDataLakeStoreAccount** Cmdlet 會測試 Data Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="daf5e-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="daf5e-107">例子</span><span class="sxs-lookup"><span data-stu-id="daf5e-107">EXAMPLES</span></span>

### <span data-ttu-id="daf5e-108">範例 1：測試帳戶</span><span class="sxs-lookup"><span data-stu-id="daf5e-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="daf5e-109">此命令會測試名為 ContosoADL 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="daf5e-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="daf5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="daf5e-110">PARAMETERS</span></span>

### <span data-ttu-id="daf5e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf5e-111">-DefaultProfile</span></span>
<span data-ttu-id="daf5e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="daf5e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daf5e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="daf5e-113">-Name</span></span>
<span data-ttu-id="daf5e-114">指定要測試的 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="daf5e-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf5e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf5e-115">-ResourceGroupName</span></span>
<span data-ttu-id="daf5e-116">指定包含要測試之帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="daf5e-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="daf5e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf5e-117">CommonParameters</span></span>
<span data-ttu-id="daf5e-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="daf5e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf5e-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="daf5e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf5e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="daf5e-120">INPUTS</span></span>

### <span data-ttu-id="daf5e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="daf5e-121">System.String</span></span>

## <span data-ttu-id="daf5e-122">輸出</span><span class="sxs-lookup"><span data-stu-id="daf5e-122">OUTPUTS</span></span>

### <span data-ttu-id="daf5e-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="daf5e-123">System.Boolean</span></span>

## <span data-ttu-id="daf5e-124">筆記</span><span class="sxs-lookup"><span data-stu-id="daf5e-124">NOTES</span></span>

## <span data-ttu-id="daf5e-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="daf5e-125">RELATED LINKS</span></span>

[<span data-ttu-id="daf5e-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="daf5e-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="daf5e-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="daf5e-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="daf5e-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="daf5e-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="daf5e-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="daf5e-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


