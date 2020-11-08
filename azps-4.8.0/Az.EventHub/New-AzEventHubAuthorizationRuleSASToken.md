---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrulesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRuleSASToken.md
ms.openlocfilehash: 24348c44ef9b529507c50a689f181739d1474e22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129537"
---
# <span data-ttu-id="53774-101">New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="53774-101">New-AzEventHubAuthorizationRuleSASToken</span></span>

## <span data-ttu-id="53774-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53774-102">SYNOPSIS</span></span>
<span data-ttu-id="53774-103">針對命名空間/eventhub 的 Azure eventhub 授權規則產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="53774-103">Generates a SAS token for Azure eventhub authorization rule of namespace/eventhub.</span></span> 

## <span data-ttu-id="53774-104">句法</span><span class="sxs-lookup"><span data-stu-id="53774-104">SYNTAX</span></span>

```
New-AzEventHubAuthorizationRuleSASToken [-AuthorizationRuleId] <String> [-KeyType] <String>
 [-ExpiryTime] <DateTime> [-StartTime <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53774-105">說明</span><span class="sxs-lookup"><span data-stu-id="53774-105">DESCRIPTION</span></span>
<span data-ttu-id="53774-106">New-AzEventHubAuthorizationRuleSASToken Cmdlet 會針對 Azure Eventhub Namesapce 或 Azure Eventhub 產生共用存取簽名 (SAS) 權杖</span><span class="sxs-lookup"><span data-stu-id="53774-106">The New-AzEventHubAuthorizationRuleSASToken cmdlet generates a Shared Access Signature (SAS) token for an Azure Eventhub Namesapce or Azure Eventhub</span></span>

## <span data-ttu-id="53774-107">示例</span><span class="sxs-lookup"><span data-stu-id="53774-107">EXAMPLES</span></span>

### <span data-ttu-id="53774-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53774-108">Example 1</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime -StartTime $StartTime
```

<span data-ttu-id="53774-109">針對具有開始和到期時間的命名空間，產生指定 authorixation 規則的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="53774-109">Generate SAS token for the given authorixation rule for Namespace with start and expiry time..</span></span>

### <span data-ttu-id="53774-110">範例2</span><span class="sxs-lookup"><span data-stu-id="53774-110">Example 2</span></span>
```powershell
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> $SasToken = New-AzEventHubAuthorizationRuleSASToken -AuthorizationRuleId $updatedAuthRule.Id  -KeyType Primary -ExpiryTime $EndTime
```

<span data-ttu-id="53774-111">針對具有到期時間的命名空間，為指定的 authorixation 規則產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="53774-111">Generate SAS token for the given authorixation rule for Namespace with expiry time.</span></span>

## <span data-ttu-id="53774-112">參數</span><span class="sxs-lookup"><span data-stu-id="53774-112">PARAMETERS</span></span>

### <span data-ttu-id="53774-113">-AuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="53774-113">-AuthorizationRuleId</span></span>
<span data-ttu-id="53774-114">Authoraization 規則的 ARM ResourceId</span><span class="sxs-lookup"><span data-stu-id="53774-114">ARM ResourceId of the Authoraization Rule</span></span>

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

### <span data-ttu-id="53774-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53774-115">-DefaultProfile</span></span>
<span data-ttu-id="53774-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53774-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53774-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="53774-117">-ExpiryTime</span></span>
<span data-ttu-id="53774-118">到期時間</span><span class="sxs-lookup"><span data-stu-id="53774-118">Expiry Time</span></span>

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

### <span data-ttu-id="53774-119">-KeyType</span><span class="sxs-lookup"><span data-stu-id="53774-119">-KeyType</span></span>
<span data-ttu-id="53774-120">金鑰類型</span><span class="sxs-lookup"><span data-stu-id="53774-120">Key Type</span></span>

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

### <span data-ttu-id="53774-121">-StartTime</span><span class="sxs-lookup"><span data-stu-id="53774-121">-StartTime</span></span>
<span data-ttu-id="53774-122">開始時間</span><span class="sxs-lookup"><span data-stu-id="53774-122">Start Time</span></span>

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

### <span data-ttu-id="53774-123">-確認</span><span class="sxs-lookup"><span data-stu-id="53774-123">-Confirm</span></span>
<span data-ttu-id="53774-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53774-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53774-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53774-125">-WhatIf</span></span>
<span data-ttu-id="53774-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53774-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53774-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53774-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53774-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53774-128">CommonParameters</span></span>
<span data-ttu-id="53774-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53774-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="53774-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53774-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53774-131">輸入</span><span class="sxs-lookup"><span data-stu-id="53774-131">INPUTS</span></span>

### <span data-ttu-id="53774-132">System.object</span><span class="sxs-lookup"><span data-stu-id="53774-132">System.String</span></span>

### <span data-ttu-id="53774-133">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="53774-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="53774-134">輸出</span><span class="sxs-lookup"><span data-stu-id="53774-134">OUTPUTS</span></span>

### <span data-ttu-id="53774-135">PSSharedAccessSignatureAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="53774-135">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessSignatureAttributes</span></span>

## <span data-ttu-id="53774-136">筆記</span><span class="sxs-lookup"><span data-stu-id="53774-136">NOTES</span></span>

## <span data-ttu-id="53774-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="53774-137">RELATED LINKS</span></span>