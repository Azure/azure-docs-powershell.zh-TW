---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: fc0cc8acf45403593124135cab87072a719f291d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904322"
---
# <span data-ttu-id="c617d-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c617d-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="c617d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c617d-102">SYNOPSIS</span></span>
<span data-ttu-id="c617d-103">{{Fill in The Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="c617d-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="c617d-104">語法</span><span class="sxs-lookup"><span data-stu-id="c617d-104">SYNTAX</span></span>

### <span data-ttu-id="c617d-105">MigrationConfigurationPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c617d-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c617d-106">命名空間InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c617d-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c617d-107">命名空間ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c617d-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c617d-108">描述</span><span class="sxs-lookup"><span data-stu-id="c617d-108">DESCRIPTION</span></span>
<span data-ttu-id="c617d-109">**Stop-AzServiceBusMigration Cmdlet** 終止標準到進位命名空間之間的移轉</span><span class="sxs-lookup"><span data-stu-id="c617d-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="c617d-110">例子</span><span class="sxs-lookup"><span data-stu-id="c617d-110">EXAMPLES</span></span>

### <span data-ttu-id="c617d-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c617d-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="c617d-112">Cmdlet 會終止在建立移轉組時所提供的標準命名空間和進一步命名空間之間的移轉。</span><span class="sxs-lookup"><span data-stu-id="c617d-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="c617d-113">參數</span><span class="sxs-lookup"><span data-stu-id="c617d-113">PARAMETERS</span></span>

### <span data-ttu-id="c617d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c617d-114">-DefaultProfile</span></span>
<span data-ttu-id="c617d-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c617d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c617d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c617d-116">-InputObject</span></span>
<span data-ttu-id="c617d-117">Service Bus Migration Configuration Standard 命名空間物件</span><span class="sxs-lookup"><span data-stu-id="c617d-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c617d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c617d-118">-Name</span></span>
<span data-ttu-id="c617d-119">標準命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="c617d-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c617d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c617d-120">-PassThru</span></span>
<span data-ttu-id="c617d-121">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="c617d-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c617d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c617d-122">-ResourceGroupName</span></span>
<span data-ttu-id="c617d-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="c617d-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c617d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c617d-124">-ResourceId</span></span>
<span data-ttu-id="c617d-125">Service Bus Migration Configuration Standard 命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c617d-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c617d-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c617d-126">-Confirm</span></span>
<span data-ttu-id="c617d-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c617d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c617d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c617d-128">-WhatIf</span></span>
<span data-ttu-id="c617d-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c617d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c617d-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c617d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c617d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c617d-131">CommonParameters</span></span>
<span data-ttu-id="c617d-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c617d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c617d-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c617d-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c617d-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c617d-134">INPUTS</span></span>

### <span data-ttu-id="c617d-135">Microsoft.Azure.Commands.ServiceBus.models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c617d-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="c617d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c617d-136">System.String</span></span>

## <span data-ttu-id="c617d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c617d-137">OUTPUTS</span></span>

### <span data-ttu-id="c617d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c617d-138">System.Boolean</span></span>

## <span data-ttu-id="c617d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c617d-139">NOTES</span></span>

## <span data-ttu-id="c617d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c617d-140">RELATED LINKS</span></span>
