---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ba81e987e19d6698c8ea1d9e489d353d58007aea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614628"
---
# <span data-ttu-id="0679f-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0679f-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="0679f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0679f-102">SYNOPSIS</span></span>
<span data-ttu-id="0679f-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0679f-103">Gets a Storage account.</span></span>

## <span data-ttu-id="0679f-104">句法</span><span class="sxs-lookup"><span data-stu-id="0679f-104">SYNTAX</span></span>

### <span data-ttu-id="0679f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0679f-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0679f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0679f-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0679f-107">說明</span><span class="sxs-lookup"><span data-stu-id="0679f-107">DESCRIPTION</span></span>
<span data-ttu-id="0679f-108">**AzStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0679f-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="0679f-109">示例</span><span class="sxs-lookup"><span data-stu-id="0679f-109">EXAMPLES</span></span>

### <span data-ttu-id="0679f-110">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0679f-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="0679f-111">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0679f-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="0679f-112">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0679f-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="0679f-113">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0679f-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="0679f-114">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="0679f-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="0679f-115">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="0679f-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="0679f-116">參數</span><span class="sxs-lookup"><span data-stu-id="0679f-116">PARAMETERS</span></span>

### <span data-ttu-id="0679f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0679f-117">-DefaultProfile</span></span>
<span data-ttu-id="0679f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0679f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0679f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0679f-119">-Name</span></span>
<span data-ttu-id="0679f-120">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0679f-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="0679f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0679f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0679f-122">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0679f-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="0679f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0679f-123">CommonParameters</span></span>
<span data-ttu-id="0679f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0679f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0679f-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0679f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0679f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0679f-126">INPUTS</span></span>

### <span data-ttu-id="0679f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="0679f-127">System.String</span></span>

## <span data-ttu-id="0679f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0679f-128">OUTPUTS</span></span>

### <span data-ttu-id="0679f-129">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="0679f-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0679f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0679f-130">NOTES</span></span>

## <span data-ttu-id="0679f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="0679f-131">RELATED LINKS</span></span>

[<span data-ttu-id="0679f-132">新-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0679f-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="0679f-133">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0679f-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="0679f-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0679f-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

