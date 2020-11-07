---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623418"
---
# <span data-ttu-id="f2716-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f2716-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="f2716-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2716-102">SYNOPSIS</span></span>
<span data-ttu-id="f2716-103">測試資料 Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="f2716-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2716-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2716-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2716-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2716-105">DESCRIPTION</span></span>
<span data-ttu-id="f2716-106">**Test AzureRmDataLakeStoreAccount** Cmdlet 會測試資料 Lake store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="f2716-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="f2716-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2716-107">EXAMPLES</span></span>

### <span data-ttu-id="f2716-108">範例1：測試帳戶</span><span class="sxs-lookup"><span data-stu-id="f2716-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="f2716-109">這個命令會測試名為 ContosoADL 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="f2716-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="f2716-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2716-110">PARAMETERS</span></span>

### <span data-ttu-id="f2716-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2716-111">-DefaultProfile</span></span>
<span data-ttu-id="f2716-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f2716-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2716-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2716-113">-Name</span></span>
<span data-ttu-id="f2716-114">指定要測試的資料 Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2716-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="f2716-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2716-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2716-116">指定包含要測試之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2716-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="f2716-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2716-117">CommonParameters</span></span>
<span data-ttu-id="f2716-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2716-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2716-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2716-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2716-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f2716-120">INPUTS</span></span>

### <span data-ttu-id="f2716-121">System.object</span><span class="sxs-lookup"><span data-stu-id="f2716-121">System.String</span></span>

## <span data-ttu-id="f2716-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f2716-122">OUTPUTS</span></span>

### <span data-ttu-id="f2716-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f2716-123">System.Boolean</span></span>

## <span data-ttu-id="f2716-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f2716-124">NOTES</span></span>

## <span data-ttu-id="f2716-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2716-125">RELATED LINKS</span></span>

[<span data-ttu-id="f2716-126">AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f2716-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f2716-127">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f2716-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f2716-128">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f2716-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="f2716-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="f2716-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


