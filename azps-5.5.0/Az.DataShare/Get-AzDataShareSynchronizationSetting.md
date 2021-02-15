---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129430"
---
# <span data-ttu-id="d6017-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d6017-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d6017-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6017-102">SYNOPSIS</span></span>
<span data-ttu-id="d6017-103">取得共用上同步處理設定的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6017-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="d6017-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6017-104">SYNTAX</span></span>

### <span data-ttu-id="d6017-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6017-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6017-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6017-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6017-107">說明</span><span class="sxs-lookup"><span data-stu-id="d6017-107">DESCRIPTION</span></span>
<span data-ttu-id="d6017-108">**AzDataShareSynchronizationSetting** Cmdlet 會提供在共用上啟用同步處理的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6017-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="d6017-109">示例</span><span class="sxs-lookup"><span data-stu-id="d6017-109">EXAMPLES</span></span>

### <span data-ttu-id="d6017-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d6017-110">Example 1</span></span>
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

<span data-ttu-id="d6017-111">這個命令會提供在 [資料共用帳戶 WikiAds] 下的 [共用 AdsShare] 中啟用同步處理 ShareSynchronization 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6017-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="d6017-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6017-112">PARAMETERS</span></span>

### <span data-ttu-id="d6017-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6017-113">-AccountName</span></span>
<span data-ttu-id="d6017-114">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d6017-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6017-115">-DefaultProfile</span></span>
<span data-ttu-id="d6017-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6017-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6017-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-117">-Name</span></span>
<span data-ttu-id="d6017-118">同步處理設定的名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="d6017-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6017-119">-ResourceGroupName</span></span>
<span data-ttu-id="d6017-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="d6017-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6017-121">-ResourceId</span></span>
<span data-ttu-id="d6017-122">Azure 資料共用同步處理設定的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d6017-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="d6017-123">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-123">-ShareName</span></span>
<span data-ttu-id="d6017-124">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="d6017-124">Azure data share name</span></span>

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

### <span data-ttu-id="d6017-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6017-125">CommonParameters</span></span>
<span data-ttu-id="d6017-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6017-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6017-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6017-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6017-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d6017-128">INPUTS</span></span>

### <span data-ttu-id="d6017-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d6017-129">System.String</span></span>

## <span data-ttu-id="d6017-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d6017-130">OUTPUTS</span></span>

### <span data-ttu-id="d6017-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="d6017-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="d6017-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d6017-132">NOTES</span></span>

## <span data-ttu-id="d6017-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6017-133">RELATED LINKS</span></span>
