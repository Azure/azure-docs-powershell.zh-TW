---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901618"
---
# <span data-ttu-id="fc562-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc562-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="fc562-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc562-102">SYNOPSIS</span></span>
<span data-ttu-id="fc562-103">修改指定訂閱的目前儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fc562-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="fc562-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc562-104">SYNTAX</span></span>

### <span data-ttu-id="fc562-105">使用ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc562-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc562-106">使用StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fc562-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc562-107">描述</span><span class="sxs-lookup"><span data-stu-id="fc562-107">DESCRIPTION</span></span>
<span data-ttu-id="fc562-108">**Set-AzCurrentStorageAccount** Cmdlet 會修改 Azure PowerShell 中指定 Azure 訂閱的目前 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fc562-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="fc562-109">當您存取儲存空間而不指定儲存空間帳戶名稱時，會使用目前的儲存空間帳戶做為預設值。</span><span class="sxs-lookup"><span data-stu-id="fc562-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="fc562-110">例子</span><span class="sxs-lookup"><span data-stu-id="fc562-110">EXAMPLES</span></span>

### <span data-ttu-id="fc562-111">範例 1：設定目前的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="fc562-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="fc562-112">此命令會設定指定訂閱的預設儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="fc562-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="fc562-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc562-113">PARAMETERS</span></span>

### <span data-ttu-id="fc562-114">-內容</span><span class="sxs-lookup"><span data-stu-id="fc562-114">-Context</span></span>
<span data-ttu-id="fc562-115">指定目前儲存空間帳戶的 **AzureStorageCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fc562-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="fc562-116">若要取得儲存內容物件，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc562-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc562-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc562-117">-DefaultProfile</span></span>
<span data-ttu-id="fc562-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc562-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc562-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc562-119">-Name</span></span>
<span data-ttu-id="fc562-120">指定此 Cmdlet 修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fc562-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc562-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc562-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc562-122">指定包含要修改的儲存空間帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="fc562-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc562-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc562-123">CommonParameters</span></span>
<span data-ttu-id="fc562-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc562-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc562-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fc562-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc562-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fc562-126">INPUTS</span></span>

### <span data-ttu-id="fc562-127">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="fc562-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="fc562-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fc562-128">System.String</span></span>

## <span data-ttu-id="fc562-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fc562-129">OUTPUTS</span></span>

### <span data-ttu-id="fc562-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fc562-130">System.String</span></span>

## <span data-ttu-id="fc562-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fc562-131">NOTES</span></span>

## <span data-ttu-id="fc562-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc562-132">RELATED LINKS</span></span>

[<span data-ttu-id="fc562-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fc562-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


