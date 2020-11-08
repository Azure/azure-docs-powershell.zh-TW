---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970443"
---
# <span data-ttu-id="d7c64-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="d7c64-101">New-AzActionGroup</span></span>

## <span data-ttu-id="d7c64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d7c64-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c64-103">在記憶體中建立 ActionGroup 參考物件。</span><span class="sxs-lookup"><span data-stu-id="d7c64-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="d7c64-104">句法</span><span class="sxs-lookup"><span data-stu-id="d7c64-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7c64-105">說明</span><span class="sxs-lookup"><span data-stu-id="d7c64-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c64-106">**新的 AzActionGroup** Cmdlet 會在記憶體中建立動作群組參照物件。</span><span class="sxs-lookup"><span data-stu-id="d7c64-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="d7c64-107">示例</span><span class="sxs-lookup"><span data-stu-id="d7c64-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c64-108">範例1：在記憶體中建立動作群組參照物件</span><span class="sxs-lookup"><span data-stu-id="d7c64-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="d7c64-109">參數</span><span class="sxs-lookup"><span data-stu-id="d7c64-109">PARAMETERS</span></span>

### <span data-ttu-id="d7c64-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="d7c64-110">-ActionGroupId</span></span>
<span data-ttu-id="d7c64-111">動作群組的識別碼/名稱。</span><span class="sxs-lookup"><span data-stu-id="d7c64-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c64-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c64-112">-DefaultProfile</span></span>
<span data-ttu-id="d7c64-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d7c64-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7c64-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="d7c64-114">-WebhookProperty</span></span>
<span data-ttu-id="d7c64-115">[動作] 群組的 webhook 屬性</span><span class="sxs-lookup"><span data-stu-id="d7c64-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7c64-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c64-116">CommonParameters</span></span>
<span data-ttu-id="d7c64-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d7c64-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c64-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d7c64-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c64-119">輸入</span><span class="sxs-lookup"><span data-stu-id="d7c64-119">INPUTS</span></span>

### <span data-ttu-id="d7c64-120">System.object</span><span class="sxs-lookup"><span data-stu-id="d7c64-120">System.String</span></span>

### <span data-ttu-id="d7c64-121">[System.object]。字典 ' 2 [CoreLib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]，[System.object，，Culture = 中立，PublicKeyToken = 4.0.0.0]」）。））中的 "</span><span class="sxs-lookup"><span data-stu-id="d7c64-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d7c64-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d7c64-122">OUTPUTS</span></span>

### <span data-ttu-id="d7c64-123">ActivityLogAlertActionGroup 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="d7c64-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="d7c64-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d7c64-124">NOTES</span></span>

## <span data-ttu-id="d7c64-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7c64-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7c64-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d7c64-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="d7c64-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d7c64-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="d7c64-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d7c64-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="d7c64-129">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d7c64-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="d7c64-130">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d7c64-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="d7c64-131">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="d7c64-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)
