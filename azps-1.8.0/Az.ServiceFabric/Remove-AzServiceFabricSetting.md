---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 22cc09a405d124ef4bf44342077b53dc64f974b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620551"
---
# <span data-ttu-id="85da1-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="85da1-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="85da1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85da1-102">SYNOPSIS</span></span>
<span data-ttu-id="85da1-103">從群集中移除一或多個服務結構設定。</span><span class="sxs-lookup"><span data-stu-id="85da1-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="85da1-104">句法</span><span class="sxs-lookup"><span data-stu-id="85da1-104">SYNTAX</span></span>

### <span data-ttu-id="85da1-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="85da1-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85da1-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="85da1-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85da1-107">說明</span><span class="sxs-lookup"><span data-stu-id="85da1-107">DESCRIPTION</span></span>
<span data-ttu-id="85da1-108">使用 **移除-AzServiceFabricSetting** 從群集中移除 Service Fabric 設定。</span><span class="sxs-lookup"><span data-stu-id="85da1-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="85da1-109">示例</span><span class="sxs-lookup"><span data-stu-id="85da1-109">EXAMPLES</span></span>

### <span data-ttu-id="85da1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="85da1-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="85da1-111">此命令會移除 [EseStore] 區段下的 [MaxCursors] 設定。</span><span class="sxs-lookup"><span data-stu-id="85da1-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="85da1-112">參數</span><span class="sxs-lookup"><span data-stu-id="85da1-112">PARAMETERS</span></span>

### <span data-ttu-id="85da1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85da1-113">-DefaultProfile</span></span>
<span data-ttu-id="85da1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85da1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85da1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="85da1-115">-Name</span></span>
<span data-ttu-id="85da1-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="85da1-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85da1-117">-參數</span><span class="sxs-lookup"><span data-stu-id="85da1-117">-Parameter</span></span>
<span data-ttu-id="85da1-118">參數.</span><span class="sxs-lookup"><span data-stu-id="85da1-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85da1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85da1-119">-ResourceGroupName</span></span>
<span data-ttu-id="85da1-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85da1-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85da1-121">區段</span><span class="sxs-lookup"><span data-stu-id="85da1-121">-Section</span></span>
<span data-ttu-id="85da1-122">頂部.</span><span class="sxs-lookup"><span data-stu-id="85da1-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85da1-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="85da1-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="85da1-124">用戶端驗證類型。</span><span class="sxs-lookup"><span data-stu-id="85da1-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85da1-125">-確認</span><span class="sxs-lookup"><span data-stu-id="85da1-125">-Confirm</span></span>
<span data-ttu-id="85da1-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85da1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85da1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85da1-127">-WhatIf</span></span>
<span data-ttu-id="85da1-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85da1-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85da1-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85da1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85da1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85da1-130">CommonParameters</span></span>
<span data-ttu-id="85da1-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85da1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85da1-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85da1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85da1-133">輸入</span><span class="sxs-lookup"><span data-stu-id="85da1-133">INPUTS</span></span>

### <span data-ttu-id="85da1-134">System.object</span><span class="sxs-lookup"><span data-stu-id="85da1-134">System.String</span></span>

### <span data-ttu-id="85da1-135">PSSettingsSectionDescription [] 的 ServiceFabric []</span><span class="sxs-lookup"><span data-stu-id="85da1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="85da1-136">輸出</span><span class="sxs-lookup"><span data-stu-id="85da1-136">OUTPUTS</span></span>

### <span data-ttu-id="85da1-137">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="85da1-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="85da1-138">筆記</span><span class="sxs-lookup"><span data-stu-id="85da1-138">NOTES</span></span>

## <span data-ttu-id="85da1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="85da1-139">RELATED LINKS</span></span>
