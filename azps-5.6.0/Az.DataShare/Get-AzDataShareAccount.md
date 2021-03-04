---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 7b47e54076441f1f4e78ec8cabc6a9dd3cd47153
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902605"
---
# <span data-ttu-id="642bd-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="642bd-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="642bd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="642bd-102">SYNOPSIS</span></span>
<span data-ttu-id="642bd-103">獲得 DataShare 帳戶相關資訊</span><span class="sxs-lookup"><span data-stu-id="642bd-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="642bd-104">語法</span><span class="sxs-lookup"><span data-stu-id="642bd-104">SYNTAX</span></span>

### <span data-ttu-id="642bd-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="642bd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="642bd-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="642bd-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="642bd-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="642bd-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="642bd-108">描述</span><span class="sxs-lookup"><span data-stu-id="642bd-108">DESCRIPTION</span></span>
<span data-ttu-id="642bd-109">**Get-AzDataShareAccount** Cmdlet 會取得 Azure 訂閱/資源群組中資料共用帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="642bd-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="642bd-110">如果您指定帳戶的名稱，此 Cmdlet 會獲得該 datshare 帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="642bd-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="642bd-111">如果您未指定名稱，此 Cmdlet 會獲得 Azure 訂閱/資源群組中所有資料共用帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="642bd-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="642bd-112">例子</span><span class="sxs-lookup"><span data-stu-id="642bd-112">EXAMPLES</span></span>

### <span data-ttu-id="642bd-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="642bd-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="642bd-114">此命令會顯示 Azure 訂閱中所有資料共用帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="642bd-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="642bd-115">參數</span><span class="sxs-lookup"><span data-stu-id="642bd-115">PARAMETERS</span></span>

### <span data-ttu-id="642bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642bd-116">-DefaultProfile</span></span>
<span data-ttu-id="642bd-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="642bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642bd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="642bd-118">-Name</span></span>
<span data-ttu-id="642bd-119">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="642bd-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="642bd-121">Azure 資料共用帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="642bd-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="642bd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="642bd-122">-ResourceId</span></span>
<span data-ttu-id="642bd-123">Azure 資料共用帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="642bd-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="642bd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642bd-124">CommonParameters</span></span>
<span data-ttu-id="642bd-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="642bd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642bd-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="642bd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642bd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="642bd-127">INPUTS</span></span>

### <span data-ttu-id="642bd-128">System.String</span><span class="sxs-lookup"><span data-stu-id="642bd-128">System.String</span></span>

## <span data-ttu-id="642bd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="642bd-129">OUTPUTS</span></span>

### <span data-ttu-id="642bd-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="642bd-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="642bd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="642bd-131">NOTES</span></span>

## <span data-ttu-id="642bd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="642bd-132">RELATED LINKS</span></span>
