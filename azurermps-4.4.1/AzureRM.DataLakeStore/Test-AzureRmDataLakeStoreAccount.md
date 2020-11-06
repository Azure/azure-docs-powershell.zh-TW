---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456723"
---
# <span data-ttu-id="58cd4-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="58cd4-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="58cd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="58cd4-103">測試資料 Lake Store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="58cd4-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58cd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="58cd4-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58cd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="58cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="58cd4-106">**Test AzureRmDataLakeStoreAccount** Cmdlet 會測試資料 Lake store 帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="58cd4-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="58cd4-107">示例</span><span class="sxs-lookup"><span data-stu-id="58cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="58cd4-108">範例1：測試帳戶</span><span class="sxs-lookup"><span data-stu-id="58cd4-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="58cd4-109">這個命令會測試名為 ContosoADL 的帳戶是否存在。</span><span class="sxs-lookup"><span data-stu-id="58cd4-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="58cd4-110">參數</span><span class="sxs-lookup"><span data-stu-id="58cd4-110">PARAMETERS</span></span>

### <span data-ttu-id="58cd4-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="58cd4-111">-Name</span></span>
<span data-ttu-id="58cd4-112">指定要測試的資料 Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="58cd4-112">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="58cd4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cd4-113">-ResourceGroupName</span></span>
<span data-ttu-id="58cd4-114">指定包含要測試之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58cd4-114">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="58cd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cd4-115">-DefaultProfile</span></span>
<span data-ttu-id="58cd4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58cd4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58cd4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cd4-117">CommonParameters</span></span>
<span data-ttu-id="58cd4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58cd4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cd4-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58cd4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cd4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="58cd4-120">INPUTS</span></span>

## <span data-ttu-id="58cd4-121">輸出</span><span class="sxs-lookup"><span data-stu-id="58cd4-121">OUTPUTS</span></span>

### <span data-ttu-id="58cd4-122">bool</span><span class="sxs-lookup"><span data-stu-id="58cd4-122">bool</span></span>
<span data-ttu-id="58cd4-123">True 或 false，表示已存在指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="58cd4-123">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="58cd4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="58cd4-124">NOTES</span></span>

## <span data-ttu-id="58cd4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="58cd4-125">RELATED LINKS</span></span>

[<span data-ttu-id="58cd4-126">AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="58cd4-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="58cd4-127">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="58cd4-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="58cd4-128">移除-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="58cd4-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="58cd4-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="58cd4-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


