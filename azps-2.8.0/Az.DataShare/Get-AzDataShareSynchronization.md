---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: f211579d98957f48a389ad10c6044c6193ad9993
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612665"
---
# <span data-ttu-id="f9dbc-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f9dbc-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="f9dbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dbc-103">取得共用的同步處理設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="f9dbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9dbc-104">SYNTAX</span></span>

### <span data-ttu-id="f9dbc-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9dbc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dbc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dbc-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9dbc-107">說明</span><span class="sxs-lookup"><span data-stu-id="f9dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="f9dbc-108">**AzDataShareSynchronization** Cmdlet 會提供有關資料共用帳戶下共用中所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="f9dbc-109">示例</span><span class="sxs-lookup"><span data-stu-id="f9dbc-109">EXAMPLES</span></span>

### <span data-ttu-id="f9dbc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f9dbc-110">Example 1</span></span>
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

<span data-ttu-id="f9dbc-111">這個命令會提供在資料共用帳戶 WikiAds 中，在 [共用 AdsShare] 中所提供的所有同步處理設定的資訊。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="f9dbc-112">參數</span><span class="sxs-lookup"><span data-stu-id="f9dbc-112">PARAMETERS</span></span>

### <span data-ttu-id="f9dbc-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f9dbc-113">-AccountName</span></span>
<span data-ttu-id="f9dbc-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="f9dbc-114">Azure data share account name</span></span>

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

### <span data-ttu-id="f9dbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dbc-115">-DefaultProfile</span></span>
<span data-ttu-id="f9dbc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9dbc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dbc-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9dbc-118">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="f9dbc-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f9dbc-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9dbc-119">-ResourceId</span></span>
<span data-ttu-id="f9dbc-120">Azure 資料共用資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f9dbc-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="f9dbc-121">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="f9dbc-121">-ShareName</span></span>
<span data-ttu-id="f9dbc-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="f9dbc-122">Azure data share name</span></span>

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

### <span data-ttu-id="f9dbc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dbc-123">CommonParameters</span></span>
<span data-ttu-id="f9dbc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dbc-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9dbc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dbc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f9dbc-126">INPUTS</span></span>

### <span data-ttu-id="f9dbc-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f9dbc-127">System.String</span></span>

## <span data-ttu-id="f9dbc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f9dbc-128">OUTPUTS</span></span>

### <span data-ttu-id="f9dbc-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="f9dbc-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="f9dbc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f9dbc-130">NOTES</span></span>

## <span data-ttu-id="f9dbc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9dbc-131">RELATED LINKS</span></span>
