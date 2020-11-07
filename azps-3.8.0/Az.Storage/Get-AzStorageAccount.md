---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: db0c0672a6f60aa8c46f85a98e74f5184842cd72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958241"
---
# <span data-ttu-id="edb68-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edb68-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="edb68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="edb68-102">SYNOPSIS</span></span>
<span data-ttu-id="edb68-103">取得儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="edb68-103">Gets a Storage account.</span></span>

## <span data-ttu-id="edb68-104">句法</span><span class="sxs-lookup"><span data-stu-id="edb68-104">SYNTAX</span></span>

### <span data-ttu-id="edb68-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="edb68-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edb68-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="edb68-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edb68-107">說明</span><span class="sxs-lookup"><span data-stu-id="edb68-107">DESCRIPTION</span></span>
<span data-ttu-id="edb68-108">**AzStorageAccount** Cmdlet 會取得指定的儲存空間帳戶或資源群組或訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="edb68-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="edb68-109">示例</span><span class="sxs-lookup"><span data-stu-id="edb68-109">EXAMPLES</span></span>

### <span data-ttu-id="edb68-110">範例1：取得指定的儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="edb68-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="edb68-111">這個命令會取得指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="edb68-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="edb68-112">範例2：取得資源群組中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="edb68-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="edb68-113">這個命令會取得資源群組中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="edb68-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="edb68-114">範例3：取得訂閱中的所有儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="edb68-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="edb68-115">這個命令會取得訂閱中的所有儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="edb68-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="edb68-116">參數</span><span class="sxs-lookup"><span data-stu-id="edb68-116">PARAMETERS</span></span>

### <span data-ttu-id="edb68-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb68-117">-DefaultProfile</span></span>
<span data-ttu-id="edb68-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="edb68-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb68-119">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="edb68-119">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="edb68-120">取得儲存空間帳戶的 GeoReplicationStats。</span><span class="sxs-lookup"><span data-stu-id="edb68-120">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edb68-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="edb68-121">-Name</span></span>
<span data-ttu-id="edb68-122">指定要取得的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="edb68-122">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="edb68-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb68-123">-ResourceGroupName</span></span>
<span data-ttu-id="edb68-124">指定包含要取得之儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edb68-124">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="edb68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb68-125">CommonParameters</span></span>
<span data-ttu-id="edb68-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="edb68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb68-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="edb68-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb68-128">輸入</span><span class="sxs-lookup"><span data-stu-id="edb68-128">INPUTS</span></span>

### <span data-ttu-id="edb68-129">System.object</span><span class="sxs-lookup"><span data-stu-id="edb68-129">System.String</span></span>

## <span data-ttu-id="edb68-130">輸出</span><span class="sxs-lookup"><span data-stu-id="edb68-130">OUTPUTS</span></span>

### <span data-ttu-id="edb68-131">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="edb68-131">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="edb68-132">筆記</span><span class="sxs-lookup"><span data-stu-id="edb68-132">NOTES</span></span>

## <span data-ttu-id="edb68-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="edb68-133">RELATED LINKS</span></span>

[<span data-ttu-id="edb68-134">新-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edb68-134">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="edb68-135">移除-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edb68-135">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="edb68-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edb68-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


