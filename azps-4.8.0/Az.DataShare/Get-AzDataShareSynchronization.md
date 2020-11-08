---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129589"
---
# <span data-ttu-id="bb940-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="bb940-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="bb940-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb940-102">SYNOPSIS</span></span>
<span data-ttu-id="bb940-103">取得共用的同步處理設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bb940-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="bb940-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb940-104">SYNTAX</span></span>

### <span data-ttu-id="bb940-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bb940-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb940-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb940-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb940-107">說明</span><span class="sxs-lookup"><span data-stu-id="bb940-107">DESCRIPTION</span></span>
<span data-ttu-id="bb940-108">**AzDataShareSynchronization** Cmdlet 會提供有關資料共用帳戶下共用中所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="bb940-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="bb940-109">示例</span><span class="sxs-lookup"><span data-stu-id="bb940-109">EXAMPLES</span></span>

### <span data-ttu-id="bb940-110">範例1</span><span class="sxs-lookup"><span data-stu-id="bb940-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="bb940-111">這個命令會提供在資料共用帳戶 WikiAds 中，在 [共用 AdsShare] 中所提供的所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="bb940-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="bb940-112">參數</span><span class="sxs-lookup"><span data-stu-id="bb940-112">PARAMETERS</span></span>

### <span data-ttu-id="bb940-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bb940-113">-AccountName</span></span>
<span data-ttu-id="bb940-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="bb940-114">Azure data share account name</span></span>

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

### <span data-ttu-id="bb940-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb940-115">-DefaultProfile</span></span>
<span data-ttu-id="bb940-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb940-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb940-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb940-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb940-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="bb940-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="bb940-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb940-119">-ResourceId</span></span>
<span data-ttu-id="bb940-120">Azure 資料共用資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bb940-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="bb940-121">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="bb940-121">-ShareName</span></span>
<span data-ttu-id="bb940-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="bb940-122">Azure data share name</span></span>

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

### <span data-ttu-id="bb940-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb940-123">CommonParameters</span></span>
<span data-ttu-id="bb940-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb940-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb940-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bb940-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb940-126">輸入</span><span class="sxs-lookup"><span data-stu-id="bb940-126">INPUTS</span></span>

### <span data-ttu-id="bb940-127">System.object</span><span class="sxs-lookup"><span data-stu-id="bb940-127">System.String</span></span>

## <span data-ttu-id="bb940-128">輸出</span><span class="sxs-lookup"><span data-stu-id="bb940-128">OUTPUTS</span></span>

### <span data-ttu-id="bb940-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="bb940-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="bb940-130">筆記</span><span class="sxs-lookup"><span data-stu-id="bb940-130">NOTES</span></span>

## <span data-ttu-id="bb940-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb940-131">RELATED LINKS</span></span>
