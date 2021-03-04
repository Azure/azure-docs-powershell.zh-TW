---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebusauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRuleSASToken.md
ms.openlocfilehash: 313022f4d622058594398b72dfd917e18cfaec77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908453"
---
# <span data-ttu-id="54aa3-101">New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="54aa3-101">New-AzServiceBusAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="54aa3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54aa3-102">SYNOPSIS</span></span>
<span data-ttu-id="54aa3-103">產生 AZURE Servicebus 授權規則的 SAS tolen 命名空間/佇列/topic。</span><span class="sxs-lookup"><span data-stu-id="54aa3-103">Generates a SAS tolen for Azure servicebus authorization rule of namespace/queue/topic.</span></span> 

## <span data-ttu-id="54aa3-104">語法</span><span class="sxs-lookup"><span data-stu-id="54aa3-104">SYNTAX</span></span>

```
New-AzServiceBusAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54aa3-105">描述</span><span class="sxs-lookup"><span data-stu-id="54aa3-105">DESCRIPTION</span></span>
<span data-ttu-id="54aa3-106">Cmdlet New-AzServiceBusAuthorizationRuleSASToken Azure Eventhub Namesapce 或 Azure Eventhub 的 SAS (SAS) 權杖產生共用存取簽章</span><span class="sxs-lookup"><span data-stu-id="54aa3-106">The New-AzServiceBusAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="54aa3-107">例子</span><span class="sxs-lookup"><span data-stu-id="54aa3-107">EXAMPLES</span></span>

### <span data-ttu-id="54aa3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="54aa3-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="54aa3-109">為命名空間的給定 authorixation 規則產生 SAS 權杖，且規則為開始時間和到期日。</span><span class="sxs-lookup"><span data-stu-id="54aa3-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="54aa3-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="54aa3-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzServiceBusAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="54aa3-111">為具有到期日的命名空間之給定 authorixation 規則產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="54aa3-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="54aa3-112">參數</span><span class="sxs-lookup"><span data-stu-id="54aa3-112">PARAMETERS</span></span>

### <span data-ttu-id="54aa3-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="54aa3-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="54aa3-114">撰寫規則的 ARM ResourceId</span><span class="sxs-lookup"><span data-stu-id="54aa3-114">ARM ResourceId of the Authoraization Rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aa3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54aa3-115">-DefaultProfile</span></span>
<span data-ttu-id="54aa3-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54aa3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54aa3-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="54aa3-117">-ExpiryTime</span></span>
<span data-ttu-id="54aa3-118">到期時間</span><span class="sxs-lookup"><span data-stu-id="54aa3-118">Expiry Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aa3-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="54aa3-119">-KeyType</span></span>
<span data-ttu-id="54aa3-120">金鑰類型</span><span class="sxs-lookup"><span data-stu-id="54aa3-120">Key Type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aa3-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="54aa3-121">-StartTime</span></span>
<span data-ttu-id="54aa3-122">開始時間</span><span class="sxs-lookup"><span data-stu-id="54aa3-122">Start Time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54aa3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="54aa3-123">-Confirm</span></span>
<span data-ttu-id="54aa3-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54aa3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54aa3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54aa3-125">-WhatIf</span></span>
<span data-ttu-id="54aa3-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54aa3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54aa3-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54aa3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54aa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54aa3-128">CommonParameters</span></span>
<span data-ttu-id="54aa3-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54aa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="54aa3-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="54aa3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54aa3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="54aa3-131">INPUTS</span></span>

### <span data-ttu-id="54aa3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="54aa3-132">System.String</span></span>

### <span data-ttu-id="54aa3-133">System.Nullable'1[[System.DateTime， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="54aa3-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="54aa3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="54aa3-134">OUTPUTS</span></span>

### <span data-ttu-id="54aa3-135">Microsoft.Azure.Commands.ServiceBus.models.PSSharedAccessSignatureAttributes</span><span class="sxs-lookup"><span data-stu-id="54aa3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="54aa3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="54aa3-136">NOTES</span></span>

## <span data-ttu-id="54aa3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="54aa3-137">RELATED LINKS</span></span>