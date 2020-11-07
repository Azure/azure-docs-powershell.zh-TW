---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624821"
---
# <span data-ttu-id="4f2b0-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="4f2b0-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="4f2b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4f2b0-103">在記憶體中建立 ActionGroup 參考物件。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f2b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f2b0-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f2b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f2b0-105">DESCRIPTION</span></span>
<span data-ttu-id="4f2b0-106">**新的 AzureRmActionGroup** Cmdlet 會在記憶體中建立動作群組參照物件。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="4f2b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="4f2b0-107">EXAMPLES</span></span>

### <span data-ttu-id="4f2b0-108">範例1：在記憶體中建立動作群組參照物件</span><span class="sxs-lookup"><span data-stu-id="4f2b0-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="4f2b0-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f2b0-109">PARAMETERS</span></span>

### <span data-ttu-id="4f2b0-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="4f2b0-110">-ActionGroupId</span></span>
<span data-ttu-id="4f2b0-111">動作群組的識別碼/名稱。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="4f2b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f2b0-112">-DefaultProfile</span></span>
<span data-ttu-id="4f2b0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f2b0-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="4f2b0-114">-WebhookProperty</span></span>
<span data-ttu-id="4f2b0-115">[動作] 群組的 webhook 屬性</span><span class="sxs-lookup"><span data-stu-id="4f2b0-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="4f2b0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f2b0-116">CommonParameters</span></span>
<span data-ttu-id="4f2b0-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f2b0-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f2b0-119">輸入</span><span class="sxs-lookup"><span data-stu-id="4f2b0-119">INPUTS</span></span>

## <span data-ttu-id="4f2b0-120">輸出</span><span class="sxs-lookup"><span data-stu-id="4f2b0-120">OUTPUTS</span></span>

### <span data-ttu-id="4f2b0-121">ActivityLogAlertActionGroup 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="4f2b0-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="4f2b0-122">筆記</span><span class="sxs-lookup"><span data-stu-id="4f2b0-122">NOTES</span></span>

## <span data-ttu-id="4f2b0-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f2b0-123">RELATED LINKS</span></span>

[<span data-ttu-id="4f2b0-124">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4f2b0-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4f2b0-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4f2b0-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4f2b0-126">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4f2b0-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4f2b0-127">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4f2b0-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4f2b0-128">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4f2b0-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="4f2b0-129">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4f2b0-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

