---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 9dca6272991c67375f2764725901018c331e0ca9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612663"
---
# <span data-ttu-id="dd7b6-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="dd7b6-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="dd7b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7b6-103">取得共用上同步處理設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="dd7b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd7b6-104">SYNTAX</span></span>

### <span data-ttu-id="dd7b6-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dd7b6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd7b6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd7b6-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd7b6-107">說明</span><span class="sxs-lookup"><span data-stu-id="dd7b6-107">DESCRIPTION</span></span>
<span data-ttu-id="dd7b6-108">**AzDataShareSynchronizationSetting** Cmdlet 會提供在共用上啟用同步處理的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="dd7b6-109">示例</span><span class="sxs-lookup"><span data-stu-id="dd7b6-109">EXAMPLES</span></span>

### <span data-ttu-id="dd7b6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="dd7b6-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="dd7b6-111">這個命令會提供在 [資料共用帳戶 WikiAds] 下的 [共用 AdsShare] 中啟用同步處理 ShareSynchronization 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="dd7b6-112">參數</span><span class="sxs-lookup"><span data-stu-id="dd7b6-112">PARAMETERS</span></span>

### <span data-ttu-id="dd7b6-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd7b6-113">-AccountName</span></span>
<span data-ttu-id="dd7b6-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-114">Azure data share account name</span></span>

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

### <span data-ttu-id="dd7b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7b6-115">-DefaultProfile</span></span>
<span data-ttu-id="dd7b6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7b6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-117">-Name</span></span>
<span data-ttu-id="dd7b6-118">同步處理設定的名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="dd7b6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7b6-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd7b6-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="dd7b6-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7b6-121">-ResourceId</span></span>
<span data-ttu-id="dd7b6-122">Azure 資料共用同步處理設定的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="dd7b6-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="dd7b6-123">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-123">-ShareName</span></span>
<span data-ttu-id="dd7b6-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="dd7b6-124">Azure data share name</span></span>

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

### <span data-ttu-id="dd7b6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7b6-125">CommonParameters</span></span>
<span data-ttu-id="dd7b6-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7b6-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd7b6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7b6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dd7b6-128">INPUTS</span></span>

### <span data-ttu-id="dd7b6-129">System.object</span><span class="sxs-lookup"><span data-stu-id="dd7b6-129">System.String</span></span>

## <span data-ttu-id="dd7b6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dd7b6-130">OUTPUTS</span></span>

### <span data-ttu-id="dd7b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="dd7b6-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="dd7b6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dd7b6-132">NOTES</span></span>

## <span data-ttu-id="dd7b6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd7b6-133">RELATED LINKS</span></span>
