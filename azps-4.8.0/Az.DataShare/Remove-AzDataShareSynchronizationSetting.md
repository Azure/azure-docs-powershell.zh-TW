---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 04454028957dfee3c7d50c47341be7e979ed3a9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969267"
---
# <span data-ttu-id="a2c17-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a2c17-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a2c17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2c17-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c17-103">移除同步處理設定</span><span class="sxs-lookup"><span data-stu-id="a2c17-103">removes a synchronization setting</span></span>

## <span data-ttu-id="a2c17-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2c17-104">SYNTAX</span></span>

### <span data-ttu-id="a2c17-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a2c17-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2c17-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c17-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c17-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c17-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c17-108">說明</span><span class="sxs-lookup"><span data-stu-id="a2c17-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c17-109">**AzDataShareSynchronizationSetting** Cmdlet 會移除 datashare 同步處理設定</span><span class="sxs-lookup"><span data-stu-id="a2c17-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="a2c17-110">示例</span><span class="sxs-lookup"><span data-stu-id="a2c17-110">EXAMPLES</span></span>

### <span data-ttu-id="a2c17-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a2c17-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="a2c17-112">這個命令會從 share AdsShare 中移除名為 AdsShareSynchronizationSetting 的同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="a2c17-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="a2c17-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2c17-113">PARAMETERS</span></span>

### <span data-ttu-id="a2c17-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a2c17-114">-AccountName</span></span>
<span data-ttu-id="a2c17-115">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-115">Azure Data Share Account name</span></span>

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

### <span data-ttu-id="a2c17-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c17-116">-AsJob</span></span>
<span data-ttu-id="a2c17-117">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="a2c17-117">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c17-118">-DefaultProfile</span></span>
<span data-ttu-id="a2c17-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2c17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c17-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c17-120">-InputObject</span></span>
<span data-ttu-id="a2c17-121">Azure 資料共用同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="a2c17-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c17-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-122">-Name</span></span>
<span data-ttu-id="a2c17-123">同步處理設定名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-123">Synchronization setting name</span></span>

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

### <span data-ttu-id="a2c17-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2c17-124">-PassThru</span></span>
<span data-ttu-id="a2c17-125">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="a2c17-125">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c17-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c17-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2c17-127">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a2c17-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c17-128">-ResourceId</span></span>
<span data-ttu-id="a2c17-129">同步處理設定的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a2c17-129">The resource id of the synchronization setting</span></span>

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

### <span data-ttu-id="a2c17-130">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-130">-ShareName</span></span>
<span data-ttu-id="a2c17-131">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="a2c17-131">Azure data share name</span></span>

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

### <span data-ttu-id="a2c17-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a2c17-132">-Confirm</span></span>
<span data-ttu-id="a2c17-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2c17-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c17-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c17-134">-WhatIf</span></span>
<span data-ttu-id="a2c17-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2c17-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c17-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2c17-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c17-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c17-137">CommonParameters</span></span>
<span data-ttu-id="a2c17-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2c17-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c17-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2c17-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c17-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a2c17-140">INPUTS</span></span>

### <span data-ttu-id="a2c17-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a2c17-141">System.String</span></span>

### <span data-ttu-id="a2c17-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="a2c17-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="a2c17-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a2c17-143">OUTPUTS</span></span>

### <span data-ttu-id="a2c17-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a2c17-144">System.Boolean</span></span>

## <span data-ttu-id="a2c17-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a2c17-145">NOTES</span></span>

## <span data-ttu-id="a2c17-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2c17-146">RELATED LINKS</span></span>