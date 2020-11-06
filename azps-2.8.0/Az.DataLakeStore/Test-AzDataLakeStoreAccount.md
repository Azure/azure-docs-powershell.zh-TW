---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 887dca3fa7a2155b07cd570a92a94a25e4346541
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612732"
---
# <span data-ttu-id="e27d7-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e27d7-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e27d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e27d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e27d7-103">測試資料 Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="e27d7-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e27d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="e27d7-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e27d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="e27d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e27d7-106">**Test AzDataLakeStoreAccount** Cmdlet 會測試資料 Lake store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="e27d7-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="e27d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="e27d7-107">EXAMPLES</span></span>

### <span data-ttu-id="e27d7-108">範例1：測試帳戶</span><span class="sxs-lookup"><span data-stu-id="e27d7-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e27d7-109">這個命令會測試名為 ContosoADL 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="e27d7-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="e27d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="e27d7-110">PARAMETERS</span></span>

### <span data-ttu-id="e27d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27d7-111">-DefaultProfile</span></span>
<span data-ttu-id="e27d7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e27d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e27d7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e27d7-113">-Name</span></span>
<span data-ttu-id="e27d7-114">指定要測試的資料 Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27d7-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="e27d7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27d7-115">-ResourceGroupName</span></span>
<span data-ttu-id="e27d7-116">指定包含要測試之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27d7-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="e27d7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27d7-117">CommonParameters</span></span>
<span data-ttu-id="e27d7-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e27d7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27d7-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e27d7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27d7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e27d7-120">INPUTS</span></span>

### <span data-ttu-id="e27d7-121">System.object</span><span class="sxs-lookup"><span data-stu-id="e27d7-121">System.String</span></span>

## <span data-ttu-id="e27d7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e27d7-122">OUTPUTS</span></span>

### <span data-ttu-id="e27d7-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e27d7-123">System.Boolean</span></span>

## <span data-ttu-id="e27d7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e27d7-124">NOTES</span></span>

## <span data-ttu-id="e27d7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="e27d7-125">RELATED LINKS</span></span>

[<span data-ttu-id="e27d7-126">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e27d7-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e27d7-127">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e27d7-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e27d7-128">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e27d7-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e27d7-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e27d7-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


