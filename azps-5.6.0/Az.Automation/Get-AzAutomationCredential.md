---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: f10bd8d57cd70004ed37f16234aa72dd3a1a8ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912498"
---
# <span data-ttu-id="8dcdc-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8dcdc-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="8dcdc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8dcdc-102">SYNOPSIS</span></span>
<span data-ttu-id="8dcdc-103">獲得自動化認證。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="8dcdc-104">語法</span><span class="sxs-lookup"><span data-stu-id="8dcdc-104">SYNTAX</span></span>

### <span data-ttu-id="8dcdc-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="8dcdc-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dcdc-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8dcdc-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dcdc-107">描述</span><span class="sxs-lookup"><span data-stu-id="8dcdc-107">DESCRIPTION</span></span>
<span data-ttu-id="8dcdc-108">**Get-AzAutomationCredential Cmdlet** 會取得一或多個 Azure 自動化認證。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="8dcdc-109">根據預設，會返回所有認證。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="8dcdc-110">指定認證名稱以取得特定認證。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="8dcdc-111">為了安全，此 Cmdlet 不會退回認證密碼。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="8dcdc-112">例子</span><span class="sxs-lookup"><span data-stu-id="8dcdc-112">EXAMPLES</span></span>

### <span data-ttu-id="8dcdc-113">範例 1：取得所有認證</span><span class="sxs-lookup"><span data-stu-id="8dcdc-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8dcdc-114">此命令會獲得自動化帳戶中所有認證名稱為 Contoso17 的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8dcdc-115">範例 2：取得認證</span><span class="sxs-lookup"><span data-stu-id="8dcdc-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="8dcdc-116">此命令會針對自動化帳戶中名為 Contoso17 的認證 ContosoCredential，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8dcdc-117">參數</span><span class="sxs-lookup"><span data-stu-id="8dcdc-117">PARAMETERS</span></span>

### <span data-ttu-id="8dcdc-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8dcdc-118">-AutomationAccountName</span></span>
<span data-ttu-id="8dcdc-119">指定此 Cmdlet 會為它所取取認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="8dcdc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dcdc-120">-DefaultProfile</span></span>
<span data-ttu-id="8dcdc-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8dcdc-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dcdc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8dcdc-122">-Name</span></span>
<span data-ttu-id="8dcdc-123">指定要取回的認證名稱。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dcdc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dcdc-124">-ResourceGroupName</span></span>
<span data-ttu-id="8dcdc-125">指定此 Cmdlet 會取回認證的資源群組。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="8dcdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dcdc-126">CommonParameters</span></span>
<span data-ttu-id="8dcdc-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dcdc-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8dcdc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dcdc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8dcdc-129">INPUTS</span></span>

### <span data-ttu-id="8dcdc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8dcdc-130">System.String</span></span>

## <span data-ttu-id="8dcdc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8dcdc-131">OUTPUTS</span></span>

### <span data-ttu-id="8dcdc-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="8dcdc-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="8dcdc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8dcdc-133">NOTES</span></span>

## <span data-ttu-id="8dcdc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8dcdc-134">RELATED LINKS</span></span>

[<span data-ttu-id="8dcdc-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8dcdc-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="8dcdc-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8dcdc-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="8dcdc-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="8dcdc-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


