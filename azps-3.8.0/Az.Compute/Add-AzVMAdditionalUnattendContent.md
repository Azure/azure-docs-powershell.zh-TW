---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956238"
---
# <span data-ttu-id="a1a57-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="a1a57-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="a1a57-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1a57-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a57-103">將資訊新增至無人參與的 Windows 安裝程式應答檔。</span><span class="sxs-lookup"><span data-stu-id="a1a57-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="a1a57-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1a57-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1a57-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1a57-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a57-106">**AzVMAdditionalUnattendContent** Cmdlet 會將資訊新增到無人參與的 Windows 安裝程式應答檔案。</span><span class="sxs-lookup"><span data-stu-id="a1a57-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="a1a57-107">指定其他基64編碼的 xml 格式資訊，此 Cmdlet 會將其新增至 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="a1a57-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="a1a57-108">示例</span><span class="sxs-lookup"><span data-stu-id="a1a57-108">EXAMPLES</span></span>

### <span data-ttu-id="a1a57-109">範例1：新增內容至 unattend.xml</span><span class="sxs-lookup"><span data-stu-id="a1a57-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="a1a57-110">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1a57-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a1a57-111">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1a57-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a1a57-112">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a1a57-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a1a57-113">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="a1a57-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a1a57-114">第三個命令會使用 Get-Credential Cmdlet 來建立認證物件，然後將結果儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="a1a57-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="a1a57-115">該命令會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="a1a57-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="a1a57-116">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="a1a57-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="a1a57-117">第四個命令使用 **AzVMOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a1a57-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a1a57-118">第五個命令會將內容指派給 $AucContent 變數。</span><span class="sxs-lookup"><span data-stu-id="a1a57-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="a1a57-119">內容包含密碼。</span><span class="sxs-lookup"><span data-stu-id="a1a57-119">The content includes a password.</span></span>
<span data-ttu-id="a1a57-120">最後一個命令會將儲存在 $AucContent 的內容新增到 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="a1a57-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="a1a57-121">參數</span><span class="sxs-lookup"><span data-stu-id="a1a57-121">PARAMETERS</span></span>

### <span data-ttu-id="a1a57-122">-內容</span><span class="sxs-lookup"><span data-stu-id="a1a57-122">-Content</span></span>
<span data-ttu-id="a1a57-123">指定基本64編碼格式的 XML 格式化內容。</span><span class="sxs-lookup"><span data-stu-id="a1a57-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="a1a57-124">這個 Cmdlet 會將內容新增至 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="a1a57-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="a1a57-125">XML 內容必須小於 4 KB，且必須包含此 Cmdlet 插入之設定或功能的根項目。</span><span class="sxs-lookup"><span data-stu-id="a1a57-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a57-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a57-126">-DefaultProfile</span></span>
<span data-ttu-id="a1a57-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1a57-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a57-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="a1a57-128">-SettingName</span></span>
<span data-ttu-id="a1a57-129">指定要套用內容的設定名稱。</span><span class="sxs-lookup"><span data-stu-id="a1a57-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="a1a57-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a1a57-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a1a57-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="a1a57-131">FirstLogonCommands</span></span>
- <span data-ttu-id="a1a57-132">自動</span><span class="sxs-lookup"><span data-stu-id="a1a57-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a57-133">-VM</span><span class="sxs-lookup"><span data-stu-id="a1a57-133">-VM</span></span>
<span data-ttu-id="a1a57-134">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a1a57-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="a1a57-135">若要取得虛擬機器物件，請使用 [AzVM](./Get-AzVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1a57-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="a1a57-136">使用 [New-AzVMConfig](./New-AzVMConfig.md) Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="a1a57-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1a57-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a57-137">CommonParameters</span></span>
<span data-ttu-id="a1a57-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1a57-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a57-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1a57-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a57-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a1a57-140">INPUTS</span></span>

### <span data-ttu-id="a1a57-141">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a1a57-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a1a57-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a1a57-142">System.String</span></span>

### <span data-ttu-id="a1a57-143">"SettingNames" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="a1a57-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a1a57-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a1a57-144">OUTPUTS</span></span>

### <span data-ttu-id="a1a57-145">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a1a57-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a1a57-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a1a57-146">NOTES</span></span>

## <span data-ttu-id="a1a57-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1a57-147">RELATED LINKS</span></span>

[<span data-ttu-id="a1a57-148">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a1a57-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="a1a57-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a1a57-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="a1a57-150">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a1a57-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
