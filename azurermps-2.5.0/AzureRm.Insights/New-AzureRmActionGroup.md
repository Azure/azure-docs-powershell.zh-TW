---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799942"
---
# <span data-ttu-id="864f9-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="864f9-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="864f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="864f9-102">SYNOPSIS</span></span>
<span data-ttu-id="864f9-103">在記憶體中建立 ActionGroup 參考物件。</span><span class="sxs-lookup"><span data-stu-id="864f9-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="864f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="864f9-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="864f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="864f9-105">DESCRIPTION</span></span>
<span data-ttu-id="864f9-106">**新的 AzureRmActionGroup** Cmdlet 會在記憶體中建立動作群組參照物件。</span><span class="sxs-lookup"><span data-stu-id="864f9-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="864f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="864f9-107">EXAMPLES</span></span>

### <span data-ttu-id="864f9-108">範例1：在記憶體中建立動作群組參照物件</span><span class="sxs-lookup"><span data-stu-id="864f9-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="864f9-109">參數</span><span class="sxs-lookup"><span data-stu-id="864f9-109">PARAMETERS</span></span>

### <span data-ttu-id="864f9-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="864f9-110">-ActionGroupId</span></span>
<span data-ttu-id="864f9-111">動作群組的識別碼/名稱。</span><span class="sxs-lookup"><span data-stu-id="864f9-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="864f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864f9-112">-DefaultProfile</span></span>
<span data-ttu-id="864f9-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="864f9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864f9-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="864f9-114">-WebhookProperty</span></span>
<span data-ttu-id="864f9-115">[動作] 群組的 webhook 屬性</span><span class="sxs-lookup"><span data-stu-id="864f9-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="864f9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864f9-116">CommonParameters</span></span>
<span data-ttu-id="864f9-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="864f9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864f9-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="864f9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864f9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="864f9-119">INPUTS</span></span>

### <span data-ttu-id="864f9-120">System.object</span><span class="sxs-lookup"><span data-stu-id="864f9-120">System.String</span></span>

### <span data-ttu-id="864f9-121">[System.object]。字典 "2 [" System.object = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]，[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="864f9-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="864f9-122">輸出</span><span class="sxs-lookup"><span data-stu-id="864f9-122">OUTPUTS</span></span>

### <span data-ttu-id="864f9-123">ActivityLogAlertActionGroup 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="864f9-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="864f9-124">筆記</span><span class="sxs-lookup"><span data-stu-id="864f9-124">NOTES</span></span>

## <span data-ttu-id="864f9-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="864f9-125">RELATED LINKS</span></span>

[<span data-ttu-id="864f9-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="864f9-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="864f9-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="864f9-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="864f9-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="864f9-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="864f9-129">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="864f9-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="864f9-130">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="864f9-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="864f9-131">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="864f9-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

