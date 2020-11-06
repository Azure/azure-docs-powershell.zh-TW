---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 420226346f89b480c283a190ee54f87cde2de005
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612560"
---
# <span data-ttu-id="17a35-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="17a35-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="17a35-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17a35-102">SYNOPSIS</span></span>
<span data-ttu-id="17a35-103">在 DevTest Labs 中取得 lab 的允許虛擬機器大小原則。</span><span class="sxs-lookup"><span data-stu-id="17a35-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="17a35-104">句法</span><span class="sxs-lookup"><span data-stu-id="17a35-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17a35-105">說明</span><span class="sxs-lookup"><span data-stu-id="17a35-105">DESCRIPTION</span></span>
<span data-ttu-id="17a35-106">**AzDtlAllowedVMSizesPolicy** Cmdlet 會取得允許的虛擬機器大小原則，可讓您指定實驗室所允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="17a35-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="17a35-107">Cmdlet 會傳回原則的啟用或停用狀態，以及您已在指定原則中設定的所有允許虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="17a35-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="17a35-108">示例</span><span class="sxs-lookup"><span data-stu-id="17a35-108">EXAMPLES</span></span>

## <span data-ttu-id="17a35-109">參數</span><span class="sxs-lookup"><span data-stu-id="17a35-109">PARAMETERS</span></span>

### <span data-ttu-id="17a35-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17a35-110">-DefaultProfile</span></span>
<span data-ttu-id="17a35-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="17a35-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17a35-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="17a35-112">-LabName</span></span>
<span data-ttu-id="17a35-113">指定此 Cmdlet 取得虛擬電腦大小原則之實驗的名稱。</span><span class="sxs-lookup"><span data-stu-id="17a35-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="17a35-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17a35-114">-ResourceGroupName</span></span>
<span data-ttu-id="17a35-115">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17a35-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="17a35-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17a35-116">CommonParameters</span></span>
<span data-ttu-id="17a35-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17a35-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17a35-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17a35-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17a35-119">輸入</span><span class="sxs-lookup"><span data-stu-id="17a35-119">INPUTS</span></span>

### <span data-ttu-id="17a35-120">System.object</span><span class="sxs-lookup"><span data-stu-id="17a35-120">System.String</span></span>

## <span data-ttu-id="17a35-121">輸出</span><span class="sxs-lookup"><span data-stu-id="17a35-121">OUTPUTS</span></span>

### <span data-ttu-id="17a35-122">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="17a35-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="17a35-123">筆記</span><span class="sxs-lookup"><span data-stu-id="17a35-123">NOTES</span></span>

## <span data-ttu-id="17a35-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="17a35-124">RELATED LINKS</span></span>

[<span data-ttu-id="17a35-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="17a35-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="17a35-126">Azure 開發測試實驗室 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="17a35-126">Azure Development Test Lab Cmdlets</span></span>](./Az.DevTestLabs.md)


