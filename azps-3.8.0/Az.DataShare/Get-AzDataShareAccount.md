---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: e70de343c064eadd846b2df150ef6a808b1bf044
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956905"
---
# <span data-ttu-id="08074-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="08074-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="08074-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08074-102">SYNOPSIS</span></span>
<span data-ttu-id="08074-103">取得 DataShare 帳戶的相關資訊</span><span class="sxs-lookup"><span data-stu-id="08074-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="08074-104">句法</span><span class="sxs-lookup"><span data-stu-id="08074-104">SYNTAX</span></span>

### <span data-ttu-id="08074-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="08074-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08074-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="08074-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08074-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08074-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08074-108">說明</span><span class="sxs-lookup"><span data-stu-id="08074-108">DESCRIPTION</span></span>
<span data-ttu-id="08074-109">**AzDataShareAccount** Cmdlet 會取得 Azure 訂閱/資源群組中 datashare 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08074-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="08074-110">如果您指定帳戶的名稱，此 Cmdlet 會取得該 datshare 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08074-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="08074-111">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 訂閱/資源群組中所有 datashare 帳戶的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="08074-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="08074-112">示例</span><span class="sxs-lookup"><span data-stu-id="08074-112">EXAMPLES</span></span>

### <span data-ttu-id="08074-113">範例1</span><span class="sxs-lookup"><span data-stu-id="08074-113">Example 1</span></span>
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

<span data-ttu-id="08074-114">這個命令會顯示有關 Azure 訂閱中所有 datashare 帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="08074-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="08074-115">參數</span><span class="sxs-lookup"><span data-stu-id="08074-115">PARAMETERS</span></span>

### <span data-ttu-id="08074-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08074-116">-DefaultProfile</span></span>
<span data-ttu-id="08074-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08074-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08074-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="08074-118">-Name</span></span>
<span data-ttu-id="08074-119">Azure 資料共用帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="08074-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="08074-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08074-120">-ResourceGroupName</span></span>
<span data-ttu-id="08074-121">Azure 資料共用帳戶的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="08074-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="08074-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08074-122">-ResourceId</span></span>
<span data-ttu-id="08074-123">Azure 資料共用帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="08074-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="08074-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08074-124">CommonParameters</span></span>
<span data-ttu-id="08074-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08074-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08074-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08074-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08074-127">輸入</span><span class="sxs-lookup"><span data-stu-id="08074-127">INPUTS</span></span>

### <span data-ttu-id="08074-128">System.object</span><span class="sxs-lookup"><span data-stu-id="08074-128">System.String</span></span>

## <span data-ttu-id="08074-129">輸出</span><span class="sxs-lookup"><span data-stu-id="08074-129">OUTPUTS</span></span>

### <span data-ttu-id="08074-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="08074-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="08074-131">筆記</span><span class="sxs-lookup"><span data-stu-id="08074-131">NOTES</span></span>

## <span data-ttu-id="08074-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="08074-132">RELATED LINKS</span></span>