---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 4d4e2a86bfa2974cabcc4208f7a314019f5804e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611684"
---
# <span data-ttu-id="09877-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="09877-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="09877-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09877-102">SYNOPSIS</span></span>
<span data-ttu-id="09877-103">停止在 Start-AzKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="09877-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="09877-104">句法</span><span class="sxs-lookup"><span data-stu-id="09877-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09877-105">說明</span><span class="sxs-lookup"><span data-stu-id="09877-105">DESCRIPTION</span></span>
<span data-ttu-id="09877-106">停止在 Start-AzKubernetesDashboard 中建立的 Kubectl SSH 隧道。</span><span class="sxs-lookup"><span data-stu-id="09877-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="09877-107">示例</span><span class="sxs-lookup"><span data-stu-id="09877-107">EXAMPLES</span></span>

### <span data-ttu-id="09877-108">範例1</span><span class="sxs-lookup"><span data-stu-id="09877-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="09877-109">執行 Start-AzKubernetesDashboard，以停止現有的 SSH 隧道設定。</span><span class="sxs-lookup"><span data-stu-id="09877-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="09877-110">參數</span><span class="sxs-lookup"><span data-stu-id="09877-110">PARAMETERS</span></span>

### <span data-ttu-id="09877-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09877-111">-DefaultProfile</span></span>
<span data-ttu-id="09877-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09877-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09877-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09877-113">-PassThru</span></span>
<span data-ttu-id="09877-114">如果 SSH 隧道已關閉，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="09877-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="09877-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09877-115">CommonParameters</span></span>
<span data-ttu-id="09877-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09877-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09877-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09877-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09877-118">輸入</span><span class="sxs-lookup"><span data-stu-id="09877-118">INPUTS</span></span>

### <span data-ttu-id="09877-119">所有</span><span class="sxs-lookup"><span data-stu-id="09877-119">None</span></span>

## <span data-ttu-id="09877-120">輸出</span><span class="sxs-lookup"><span data-stu-id="09877-120">OUTPUTS</span></span>

### <span data-ttu-id="09877-121">System.object</span><span class="sxs-lookup"><span data-stu-id="09877-121">System.Boolean</span></span>

## <span data-ttu-id="09877-122">筆記</span><span class="sxs-lookup"><span data-stu-id="09877-122">NOTES</span></span>

## <span data-ttu-id="09877-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="09877-123">RELATED LINKS</span></span>
