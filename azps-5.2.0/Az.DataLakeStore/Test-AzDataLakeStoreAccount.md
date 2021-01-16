---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 25837486fad8b17a272f5687129ff936f6d50a02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285103"
---
# <span data-ttu-id="0ec18-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0ec18-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="0ec18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0ec18-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec18-103">測試資料 Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="0ec18-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0ec18-104">句法</span><span class="sxs-lookup"><span data-stu-id="0ec18-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ec18-105">說明</span><span class="sxs-lookup"><span data-stu-id="0ec18-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec18-106">**Test AzDataLakeStoreAccount** Cmdlet 會測試資料 Lake store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="0ec18-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="0ec18-107">示例</span><span class="sxs-lookup"><span data-stu-id="0ec18-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec18-108">範例1：測試帳戶</span><span class="sxs-lookup"><span data-stu-id="0ec18-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="0ec18-109">這個命令會測試名為 ContosoADL 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="0ec18-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="0ec18-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ec18-110">PARAMETERS</span></span>

### <span data-ttu-id="0ec18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec18-111">-DefaultProfile</span></span>
<span data-ttu-id="0ec18-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0ec18-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ec18-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0ec18-113">-Name</span></span>
<span data-ttu-id="0ec18-114">指定要測試的資料 Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec18-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="0ec18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec18-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ec18-116">指定包含要測試之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ec18-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="0ec18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec18-117">CommonParameters</span></span>
<span data-ttu-id="0ec18-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0ec18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec18-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0ec18-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec18-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0ec18-120">INPUTS</span></span>

### <span data-ttu-id="0ec18-121">System.object</span><span class="sxs-lookup"><span data-stu-id="0ec18-121">System.String</span></span>

## <span data-ttu-id="0ec18-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0ec18-122">OUTPUTS</span></span>

### <span data-ttu-id="0ec18-123">System.object</span><span class="sxs-lookup"><span data-stu-id="0ec18-123">System.Boolean</span></span>

## <span data-ttu-id="0ec18-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0ec18-124">NOTES</span></span>

## <span data-ttu-id="0ec18-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ec18-125">RELATED LINKS</span></span>

[<span data-ttu-id="0ec18-126">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0ec18-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0ec18-127">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0ec18-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0ec18-128">移除-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0ec18-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="0ec18-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="0ec18-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


