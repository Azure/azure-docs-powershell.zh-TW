---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129568"
---
# <span data-ttu-id="dd984-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="dd984-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="dd984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd984-102">SYNOPSIS</span></span>
<span data-ttu-id="dd984-103">在 DevTest 實驗室中取得實驗室的每個使用者原則的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="dd984-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="dd984-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd984-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd984-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd984-105">DESCRIPTION</span></span>
<span data-ttu-id="dd984-106">**AzDtlVMsPerUserPolicy** Cmdlet 會取得實驗室的每個使用者原則的虛擬機器，這可讓您設定每位使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="dd984-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="dd984-107">Cmdlet 會傳回原則的啟用或停用狀態，以及您已在原則中設定的每個使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="dd984-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="dd984-108">示例</span><span class="sxs-lookup"><span data-stu-id="dd984-108">EXAMPLES</span></span>

## <span data-ttu-id="dd984-109">參數</span><span class="sxs-lookup"><span data-stu-id="dd984-109">PARAMETERS</span></span>

### <span data-ttu-id="dd984-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd984-110">-DefaultProfile</span></span>
<span data-ttu-id="dd984-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dd984-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd984-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="dd984-112">-LabName</span></span>
<span data-ttu-id="dd984-113">指定此 Cmdlet 針對每個使用者原則取得虛擬機器原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="dd984-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="dd984-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd984-114">-ResourceGroupName</span></span>
<span data-ttu-id="dd984-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd984-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="dd984-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd984-116">CommonParameters</span></span>
<span data-ttu-id="dd984-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd984-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd984-118">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd984-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd984-119">輸入</span><span class="sxs-lookup"><span data-stu-id="dd984-119">INPUTS</span></span>

### <span data-ttu-id="dd984-120">System.object</span><span class="sxs-lookup"><span data-stu-id="dd984-120">System.String</span></span>

## <span data-ttu-id="dd984-121">輸出</span><span class="sxs-lookup"><span data-stu-id="dd984-121">OUTPUTS</span></span>

### <span data-ttu-id="dd984-122">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="dd984-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="dd984-123">筆記</span><span class="sxs-lookup"><span data-stu-id="dd984-123">NOTES</span></span>

## <span data-ttu-id="dd984-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd984-124">RELATED LINKS</span></span>

[<span data-ttu-id="dd984-125">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="dd984-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


