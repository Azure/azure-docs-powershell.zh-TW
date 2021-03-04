---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/stop-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Stop-AzAksDashboard.md
ms.openlocfilehash: 633173a0ce8814ee2af9300be5b1cfc19bdf9a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907830"
---
# <span data-ttu-id="ebcf8-101">Stop-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="ebcf8-101">Stop-AzAksDashboard</span></span>

## <span data-ttu-id="ebcf8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ebcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="ebcf8-103">停止在 Start-AzKubernetesDashboard 中建立之 Kubectl SSH 的建立方式。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-103">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ebcf8-104">語法</span><span class="sxs-lookup"><span data-stu-id="ebcf8-104">SYNTAX</span></span>

```
Stop-AzAksDashboard [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebcf8-105">描述</span><span class="sxs-lookup"><span data-stu-id="ebcf8-105">DESCRIPTION</span></span>
<span data-ttu-id="ebcf8-106">停止在 Start-AzKubernetesDashboard 中建立之 Kubectl SSH 的建立方式。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-106">Stop the Kubectl SSH tunnel created in Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ebcf8-107">例子</span><span class="sxs-lookup"><span data-stu-id="ebcf8-107">EXAMPLES</span></span>

### <span data-ttu-id="ebcf8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ebcf8-108">Example 1</span></span>
```
PS C:\> Stop-AzKubernetesDashboard
```

<span data-ttu-id="ebcf8-109">執行 Start-AzKubernetesDashboard 來停止現有的 SSH 設定。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-109">Stops the existing SSH tunnel setup by executing Start-AzKubernetesDashboard.</span></span>

## <span data-ttu-id="ebcf8-110">參數</span><span class="sxs-lookup"><span data-stu-id="ebcf8-110">PARAMETERS</span></span>

### <span data-ttu-id="ebcf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebcf8-111">-DefaultProfile</span></span>
<span data-ttu-id="ebcf8-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebcf8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebcf8-113">-PassThru</span></span>
<span data-ttu-id="ebcf8-114">關閉 SSH 內建時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-114">Returns true if SSH tunnel is closed.</span></span>

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

### <span data-ttu-id="ebcf8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebcf8-115">CommonParameters</span></span>
<span data-ttu-id="ebcf8-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ebcf8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebcf8-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebcf8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebcf8-118">輸入</span><span class="sxs-lookup"><span data-stu-id="ebcf8-118">INPUTS</span></span>

### <span data-ttu-id="ebcf8-119">沒有</span><span class="sxs-lookup"><span data-stu-id="ebcf8-119">None</span></span>

## <span data-ttu-id="ebcf8-120">輸出</span><span class="sxs-lookup"><span data-stu-id="ebcf8-120">OUTPUTS</span></span>

### <span data-ttu-id="ebcf8-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ebcf8-121">System.Boolean</span></span>

## <span data-ttu-id="ebcf8-122">筆記</span><span class="sxs-lookup"><span data-stu-id="ebcf8-122">NOTES</span></span>

## <span data-ttu-id="ebcf8-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="ebcf8-123">RELATED LINKS</span></span>
