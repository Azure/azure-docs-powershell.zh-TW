---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a7780b18ba46b4a9e007eb4bb8ad84490bd73577
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612687"
---
# <span data-ttu-id="297a5-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="297a5-101">Get-AzDataShare</span></span>

## <span data-ttu-id="297a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="297a5-102">SYNOPSIS</span></span>
<span data-ttu-id="297a5-103">取得資料共用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="297a5-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="297a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="297a5-104">SYNTAX</span></span>

### <span data-ttu-id="297a5-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="297a5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="297a5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297a5-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="297a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="297a5-107">DESCRIPTION</span></span>
<span data-ttu-id="297a5-108">**AzDataShare** Cmdlet 會取得 Azure 資料共用 accoount 中資料共用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="297a5-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="297a5-109">如果您指定資料共用的名稱，此 Cmdlet 會取得該資料共用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="297a5-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="297a5-110">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資料共用帳戶中所有資料共用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="297a5-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="297a5-111">示例</span><span class="sxs-lookup"><span data-stu-id="297a5-111">EXAMPLES</span></span>

### <span data-ttu-id="297a5-112">範例1：取得特定的資料共用</span><span class="sxs-lookup"><span data-stu-id="297a5-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="297a5-113">這個命令會在 Azure 資料共用帳戶 WikiAdsAccount 和資源群組廣告中顯示資料共用 AdsShare 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="297a5-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="297a5-114">參數</span><span class="sxs-lookup"><span data-stu-id="297a5-114">PARAMETERS</span></span>

### <span data-ttu-id="297a5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="297a5-115">-AccountName</span></span>
<span data-ttu-id="297a5-116">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="297a5-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="297a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297a5-117">-DefaultProfile</span></span>
<span data-ttu-id="297a5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="297a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297a5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="297a5-119">-Name</span></span>
<span data-ttu-id="297a5-120">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="297a5-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="297a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="297a5-122">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="297a5-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="297a5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="297a5-123">-ResourceId</span></span>
<span data-ttu-id="297a5-124">Azure 資料共用的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="297a5-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="297a5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297a5-125">CommonParameters</span></span>
<span data-ttu-id="297a5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="297a5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297a5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="297a5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297a5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="297a5-128">INPUTS</span></span>

### <span data-ttu-id="297a5-129">System.object</span><span class="sxs-lookup"><span data-stu-id="297a5-129">System.String</span></span>

## <span data-ttu-id="297a5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="297a5-130">OUTPUTS</span></span>

### <span data-ttu-id="297a5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="297a5-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="297a5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="297a5-132">NOTES</span></span>

## <span data-ttu-id="297a5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="297a5-133">RELATED LINKS</span></span>
