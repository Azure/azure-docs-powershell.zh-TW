---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 5b4b71f3d108d78a15a5993556ab4e78f480170e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409149"
---
# <span data-ttu-id="72904-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="72904-101">New-AzActionGroup</span></span>

## <span data-ttu-id="72904-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72904-102">SYNOPSIS</span></span>
<span data-ttu-id="72904-103">在記憶體中建立 ActionGroup 參照物件。</span><span class="sxs-lookup"><span data-stu-id="72904-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="72904-104">語法</span><span class="sxs-lookup"><span data-stu-id="72904-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72904-105">描述</span><span class="sxs-lookup"><span data-stu-id="72904-105">DESCRIPTION</span></span>
<span data-ttu-id="72904-106">**New-AzActionGroup** Cmdlet 會建立記憶體中的動作群組參照物件。</span><span class="sxs-lookup"><span data-stu-id="72904-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="72904-107">例子</span><span class="sxs-lookup"><span data-stu-id="72904-107">EXAMPLES</span></span>

### <span data-ttu-id="72904-108">範例 1：在記憶體中建立動作群組參照物件</span><span class="sxs-lookup"><span data-stu-id="72904-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="72904-109">參數</span><span class="sxs-lookup"><span data-stu-id="72904-109">PARAMETERS</span></span>

### <span data-ttu-id="72904-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="72904-110">-ActionGroupId</span></span>
<span data-ttu-id="72904-111">動作群組的識別碼/名稱。</span><span class="sxs-lookup"><span data-stu-id="72904-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="72904-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72904-112">-DefaultProfile</span></span>
<span data-ttu-id="72904-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="72904-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72904-114">-Web上Property</span><span class="sxs-lookup"><span data-stu-id="72904-114">-WebhookProperty</span></span>
<span data-ttu-id="72904-115">動作群組的 Web 區屬性</span><span class="sxs-lookup"><span data-stu-id="72904-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="72904-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72904-116">CommonParameters</span></span>
<span data-ttu-id="72904-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72904-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72904-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72904-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72904-119">輸入</span><span class="sxs-lookup"><span data-stu-id="72904-119">INPUTS</span></span>

### <span data-ttu-id="72904-120">System.String</span><span class="sxs-lookup"><span data-stu-id="72904-120">System.String</span></span>

### <span data-ttu-id="72904-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="72904-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="72904-122">輸出</span><span class="sxs-lookup"><span data-stu-id="72904-122">OUTPUTS</span></span>

### <span data-ttu-id="72904-123">Microsoft.Azure.management.monitor.management.models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="72904-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="72904-124">筆記</span><span class="sxs-lookup"><span data-stu-id="72904-124">NOTES</span></span>

## <span data-ttu-id="72904-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="72904-125">RELATED LINKS</span></span>

[<span data-ttu-id="72904-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72904-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="72904-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72904-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="72904-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72904-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="72904-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72904-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="72904-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="72904-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)



