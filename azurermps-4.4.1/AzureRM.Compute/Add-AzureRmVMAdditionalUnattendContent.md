---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 66b3f8da0f133bf4f5c173d1cf7dbb03d8dc7795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454416"
---
# <span data-ttu-id="5093e-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="5093e-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="5093e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5093e-102">SYNOPSIS</span></span>
<span data-ttu-id="5093e-103">將資訊新增至無人參與的 Windows 安裝程式應答檔。</span><span class="sxs-lookup"><span data-stu-id="5093e-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5093e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5093e-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5093e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5093e-105">DESCRIPTION</span></span>
<span data-ttu-id="5093e-106">**AzureRmVMAdditionalUnattendContent** Cmdlet 會將資訊新增到無人參與的 Windows 安裝程式應答檔案。</span><span class="sxs-lookup"><span data-stu-id="5093e-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="5093e-107">指定其他基64編碼的 xml 格式資訊，此 Cmdlet 會將其新增至 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="5093e-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="5093e-108">示例</span><span class="sxs-lookup"><span data-stu-id="5093e-108">EXAMPLES</span></span>

### <span data-ttu-id="5093e-109">範例1：新增內容至 unattend.xml</span><span class="sxs-lookup"><span data-stu-id="5093e-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="5093e-110">第一個命令會在名為 [ResourceGroup11] 的資源群組中取得名為 AvailablitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。</span><span class="sxs-lookup"><span data-stu-id="5093e-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="5093e-111">第二個命令會建立一個虛擬電腦物件，然後將它儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="5093e-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5093e-112">該命令會將名稱和大小指派給虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5093e-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="5093e-113">虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="5093e-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="5093e-114">第三個命令會使用 Get-Credential Cmdlet 來建立認證物件，然後將結果儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="5093e-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="5093e-115">該命令會提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="5093e-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="5093e-116">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="5093e-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="5093e-117">第四個命令使用 **AzureRmVMOperatingSystem** Cmdlet 來設定儲存在 $VirtualMachine 中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5093e-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="5093e-118">第五個命令會將內容指派給 $AucContent 變數。</span><span class="sxs-lookup"><span data-stu-id="5093e-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="5093e-119">內容包含密碼。</span><span class="sxs-lookup"><span data-stu-id="5093e-119">The content includes a password.</span></span>

<span data-ttu-id="5093e-120">最後一個命令會將儲存在 $AucContent 的內容新增到 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="5093e-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="5093e-121">參數</span><span class="sxs-lookup"><span data-stu-id="5093e-121">PARAMETERS</span></span>

### <span data-ttu-id="5093e-122">-內容</span><span class="sxs-lookup"><span data-stu-id="5093e-122">-Content</span></span>
<span data-ttu-id="5093e-123">指定基本64編碼格式的 XML 格式化內容。</span><span class="sxs-lookup"><span data-stu-id="5093e-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="5093e-124">這個 Cmdlet 會將內容新增至 unattend.xml 檔案。</span><span class="sxs-lookup"><span data-stu-id="5093e-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="5093e-125">XML 內容必須小於 4 KB，且必須包含此 Cmdlet 插入之設定或功能的根項目。</span><span class="sxs-lookup"><span data-stu-id="5093e-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="5093e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5093e-126">-DefaultProfile</span></span>
<span data-ttu-id="5093e-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5093e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5093e-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="5093e-128">-SettingName</span></span>
<span data-ttu-id="5093e-129">指定要套用內容的設定名稱。</span><span class="sxs-lookup"><span data-stu-id="5093e-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="5093e-130">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5093e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5093e-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="5093e-131">FirstLogonCommands</span></span>
- <span data-ttu-id="5093e-132">自動</span><span class="sxs-lookup"><span data-stu-id="5093e-132">AutoLogon</span></span>

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

### <span data-ttu-id="5093e-133">-VM</span><span class="sxs-lookup"><span data-stu-id="5093e-133">-VM</span></span>
<span data-ttu-id="5093e-134">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="5093e-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="5093e-135">若要取得虛擬機器物件，請使用 [AzureRmVM](./Get-AzureRmVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5093e-135">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="5093e-136">使用 [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) Cmdlet 建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="5093e-136">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="5093e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5093e-137">CommonParameters</span></span>
<span data-ttu-id="5093e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5093e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5093e-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5093e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5093e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5093e-140">INPUTS</span></span>

## <span data-ttu-id="5093e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5093e-141">OUTPUTS</span></span>

## <span data-ttu-id="5093e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5093e-142">NOTES</span></span>

## <span data-ttu-id="5093e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5093e-143">RELATED LINKS</span></span>

[<span data-ttu-id="5093e-144">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5093e-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="5093e-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5093e-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5093e-146">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5093e-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
