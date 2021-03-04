---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 6fbef2bcedf4de93cd816f6a4702ee01df10d17f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903353"
---
# <span data-ttu-id="7a6ae-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7a6ae-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="7a6ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6ae-103">修改自動化認證。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="7a6ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a6ae-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a6ae-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="7a6ae-106">**Set-AzAutomationCredential Cmdlet** 在 Azure Automation 中將認證修改為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="7a6ae-107">例子</span><span class="sxs-lookup"><span data-stu-id="7a6ae-107">EXAMPLES</span></span>

### <span data-ttu-id="7a6ae-108">範例 1：更新認證</span><span class="sxs-lookup"><span data-stu-id="7a6ae-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="7a6ae-109">第一個命令會指派使用者名稱給$User變數。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="7a6ae-110">第二個命令會使用 Cmdlet 將純文字密碼轉換為ConvertTo-SecureString字串。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="7a6ae-111">該命令將該物件儲存在$Password變數中。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="7a6ae-112">第三個命令會根據$User和$Password建立認證，然後將它儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="7a6ae-113">最後一個命令會修改名為 ContosoCredential 的自動化認證，以在 $Credential。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="7a6ae-114">參數</span><span class="sxs-lookup"><span data-stu-id="7a6ae-114">PARAMETERS</span></span>

### <span data-ttu-id="7a6ae-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-115">-AutomationAccountName</span></span>
<span data-ttu-id="7a6ae-116">指定此 Cmdlet 可修改認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="7a6ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6ae-117">-DefaultProfile</span></span>
<span data-ttu-id="7a6ae-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="7a6ae-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a6ae-119">-描述</span><span class="sxs-lookup"><span data-stu-id="7a6ae-119">-Description</span></span>
<span data-ttu-id="7a6ae-120">指定此 Cmdlet 修改之認證的描述。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a6ae-121">-Name</span></span>
<span data-ttu-id="7a6ae-122">指定此 Cmdlet 修改的認證名稱。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a6ae-124">指定此 Cmdlet 會修改認證的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="7a6ae-125">-值</span><span class="sxs-lookup"><span data-stu-id="7a6ae-125">-Value</span></span>
<span data-ttu-id="7a6ae-126">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6ae-127">CommonParameters</span></span>
<span data-ttu-id="7a6ae-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6ae-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7a6ae-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6ae-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7a6ae-130">INPUTS</span></span>

### <span data-ttu-id="7a6ae-131">System.String</span><span class="sxs-lookup"><span data-stu-id="7a6ae-131">System.String</span></span>

### <span data-ttu-id="7a6ae-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="7a6ae-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="7a6ae-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7a6ae-133">OUTPUTS</span></span>

### <span data-ttu-id="7a6ae-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="7a6ae-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="7a6ae-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7a6ae-135">NOTES</span></span>

## <span data-ttu-id="7a6ae-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a6ae-136">RELATED LINKS</span></span>

[<span data-ttu-id="7a6ae-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7a6ae-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="7a6ae-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7a6ae-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="7a6ae-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="7a6ae-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


