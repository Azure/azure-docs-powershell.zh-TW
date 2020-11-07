---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624006"
---
# <span data-ttu-id="b8c7d-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c7d-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="b8c7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c7d-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8c7d-104">SYNTAX</span></span>

### <span data-ttu-id="b8c7d-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8c7d-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8c7d-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8c7d-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8c7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="b8c7d-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c7d-108">**AzureRmStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="b8c7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="b8c7d-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c7d-110">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="b8c7d-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="b8c7d-111">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="b8c7d-112">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="b8c7d-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="b8c7d-113">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="b8c7d-114">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="b8c7d-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="b8c7d-115">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="b8c7d-116">參數</span><span class="sxs-lookup"><span data-stu-id="b8c7d-116">PARAMETERS</span></span>

### <span data-ttu-id="b8c7d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8c7d-117">-Name</span></span>
<span data-ttu-id="b8c7d-118">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c7d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8c7d-120">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c7d-121">-DefaultProfile</span></span>
<span data-ttu-id="b8c7d-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c7d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c7d-123">CommonParameters</span></span>
<span data-ttu-id="b8c7d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c7d-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8c7d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c7d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="b8c7d-126">INPUTS</span></span>

## <span data-ttu-id="b8c7d-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b8c7d-127">OUTPUTS</span></span>

## <span data-ttu-id="b8c7d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b8c7d-128">NOTES</span></span>

## <span data-ttu-id="b8c7d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8c7d-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8c7d-130">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c7d-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="b8c7d-131">移除-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c7d-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="b8c7d-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8c7d-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


